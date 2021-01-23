# Random-number-word-
App that makes random word ( Doesnt work)



{ package com.example.nexttechcert
import android.os.Bundle
import com.google.android.material.floatingactionbutton.FloatingActionButton
import com.google.android.material.snackbar.Snackbar
import androidx.appcompat.app.AppCompatActivity
import android.view.Menu
import android.view.MenuItem
import android.widget.Button
import android.widget.SeekBar
import android.widget.TextView
import kotlin.random.Random

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val randombutton = findViewById<Button>(R.id.randombutton)
        val Resultstestview = findViewById<TextView>(R.id.Resultstextview)
        val seekBar = findViewById<SeekBar>(R.id.seekBar)

        randombutton.setOnClickListener {
            val rand = Random.toString(seekBar.progress)
            Resultstestview.text = rand
        }

    }
}
