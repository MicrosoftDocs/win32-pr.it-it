---
description: In questo esempio viene illustrato come serializzare e de serializzare l'input penna in vari formati.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Esempio di serializzazione input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e71eed5c91bf4fa1524cc52af163516ced0c7362d0d20b8ecf52ac1a08ccd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032269"
---
# <a name="ink-serialization-sample"></a>Esempio di serializzazione input penna

In questo esempio viene illustrato come serializzare e de serializzare l'input penna in vari formati. L'applicazione rappresenta un modulo con campi per l'immissione di nome, cognome e firma. L'utente può salvare questi dati come formato ISF (Pure Ink Serialized Format), Extensible Markup Language (XML) usando ISF con codifica Base64 o HTML, che fa riferimento all'input penna in un'immagine GIF (Ified Graphics Interchange Format) con codifica Base64. L'applicazione consente inoltre all'utente di aprire i file salvati in formato XML e ISF. Il formato ISF usa le proprietà estese per archiviare il nome e il cognome, mentre i formati XML e HTML archiviano queste informazioni in attributi personalizzati.

Questo esempio non supporta il caricamento dal formato HTML, perché HTML non è adatto per l'archiviazione di dati strutturati. Poiché i dati sono separati in nome, firma e così via, è necessario un formato che mantengono questa separazione, ad esempio XML o un altro tipo di formato di database.

HTML è molto utile in un ambiente in cui la formattazione è importante, ad esempio in un documento di elaborazione di testo. Il codice HTML salvato da questo esempio usa GIF giustificate. Queste GIF dispongono di ISF incorporato al loro interno, che mantiene la massima fedeltà dell'input penna. Un'applicazione per l'elaborazione di testo può salvare un documento contenente più tipi di dati, ad esempio immagini, tabelle, testo formattato e input penna persistenti in un formato HTML. Il rendering di questo codice HTML viene eseguito nei browser che non riconoscono l'input penna. Tuttavia, quando viene caricato in un'applicazione abilitata per l'input penna, la massima fedeltà dell'input penna originale è disponibile e può essere sottoposta a rendering, modificata o usata per il riconoscimento.

In questo esempio vengono usate le funzionalità seguenti:

-   Metodo [Load](/previous-versions/aa515768(v=msdn.10)) dell'oggetto [Ink](/previous-versions/ms569609(v=vs.100))
-   Metodo [Save](/previous-versions/aa515768(v=msdn.10)) dell'oggetto [Ink](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90))
-   Proprietà [ExtendedProperties](/previous-versions/aa515768(v=msdn.10)) [dell'oggetto](/previous-versions/ms582214(v=vs.100)) Ink

## <a name="collecting-ink"></a>Raccolta di input penna

Per prima cosa, fare riferimento all'API Tablet PC, che viene installata con Windows Vista e Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



Il costruttore crea e abilita [un inkCollector](/previous-versions/ms836493(v=msdn.10)) `ic` , , per il form.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Salvataggio di un file

Il metodo gestisce la finestra di dialogo Salva con nome, crea un flusso di file in cui salvare i dati dell'input penna e chiama il metodo save corrispondente alla scelta `SaveAsMenu_Click` dell'utente.

## <a name="saving-to-an-isf-file"></a>Salvataggio in un file ISF

Nel metodo i valori di nome e cognome vengono aggiunti alla proprietà ExtendedProperties della proprietà `SaveISF` [Ink](/previous-versions/ms836505(v=msdn.10)) dell'oggetto [InkCollector,](/previous-versions/ms836493(v=msdn.10)) prima che l'input penna venga serializzato e scritto nel file. [](/previous-versions/ms582214(v=vs.100)) Dopo la serializzazione dell'input penna, i valori di nome e cognome vengono rimossi dalla [proprietà](/previous-versions/aa515768(v=msdn.10)) ExtendedProperties dell'oggetto Ink.


```C++
byte[] isf;

// This is the ink object which is serialized
ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Store the name fields in the ink object
// These fields roundtrip through the ISF format
// Ignore empty fields since strictly empty strings 
//       cannot be stored in ExtendedProperties.
if (FirstNameBox.Text.Length > 0)
{
    inkProperties.Add(FirstName, FirstNameBox.Text);
}
if (LastNameBox.Text.Length > 0)
{
    inkProperties.Add(LastName, LastNameBox.Text);
}

// Perform the serialization
isf = ic.Ink.Save(PersistenceFormat.InkSerializedFormat);

// If the first and last names were added as extended
// properties to the ink, remove them - these properties
// are only used for the save and there is no need to
// keep them around on the ink object.
if (inkProperties.DoesPropertyExist(FirstName))
{
    inkProperties.Remove(FirstName);
}
if (inkProperties.DoesPropertyExist(LastName))
{
    inkProperties.Remove(LastName);
}

// Write the ISF to the stream
s.Write(isf,0,isf.Length);
```



## <a name="saving-to-an-xml-file"></a>Salvataggio in un file XML

Nel metodo `SaveXML` viene usato un oggetto [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) per creare e scrivere in un documento XML. Usando il metodo [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto [Ink,](/previous-versions/aa515768(v=msdn.10)) l'input penna viene prima convertito in una matrice di byte Ink Serialized Format con codifica Base64 e quindi la matrice di byte viene convertita in una stringa da scrivere nel file XML. Anche i dati di testo del modulo vengono scritti nel file XML.


```C++
// Get the base64 encoded ISF
base64ISF_bytes = ic.Ink.Save(PersistenceFormat.Base64InkSerializedFormat);

// Convert it to a String
base64ISF_string = utf8.GetString(base64ISF_bytes);

// Write the ISF containing node to the XML
xwriter.WriteElementString("Ink", base64ISF_string);

// Write the text data from the form
// Note that the names are stored as XML fields, rather
// than custom properties, so that these properties can 
// be most easily accessible if the XML is saved in a database.
xwriter.WriteElementString("FirstName",FirstNameBox.Text);
xwriter.WriteElementString("LastName",LastNameBox.Text);
```



## <a name="saving-to-an-html-file"></a>Salvataggio in un file HTML

Il metodo SaveHTML usa il rettangolo di selezione della raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) per verificare la presenza di una firma. Se la firma esiste, viene convertita nel formato GIF unificata usando il metodo [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto input penna e scritta in un file. Viene quindi fatto riferimento alla GIF nel file HTML.


```C++
if (ic.Ink.Strokes.GetBoundingBox().IsEmpty)
{
   MessageBox.Show("Unable to save empty ink in HTML persistence format.");
}
else
{
    FileStream gifFile;
    byte[] fortifiedGif = null;
    ...

    // Create a directory to store the fortified GIF which also contains ISF
    // and open the file for writing
    Directory.CreateDirectory(nameBase + "_files");
    using (FileStream gifFile = File.OpenWrite(nameBase + "_files\\signature.gif"))
    {

        // Generate the fortified GIF represenation of the ink
        fortifiedGif = ic.Ink.Save(PersistenceFormat.Gif);

        // Write and close the gif file
        gifFile.Write(fortifiedGif, 0, fortifiedGif.Length);
    }
```



## <a name="loading-a-file"></a>Caricamento di un file

Il metodo gestisce la finestra di dialogo Apri, apre il file e chiama il metodo di caricamento `OpenMenu_Click` corrispondente alla scelta dell'utente.

## <a name="loading-an-isf-file"></a>Caricamento di un file ISF

Il metodo legge il file creato in precedenza e converte la matrice `LoadISF` Byte in input penna con il [metodo](/previous-versions/aa515768(v=msdn.10)) Load dell'oggetto [Ink.](/previous-versions/ms569609(v=vs.100)) L'agente di raccolta input penna è temporaneamente disabilitato per assegnare l'oggetto Ink. Il `LoadISF` metodo controlla quindi la proprietà [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) dell'oggetto Ink per le stringhe di nome e cognome.


```C++
Ink loadedInk = new Ink();
byte[] isfBytes = new byte[s.Length];

// read in the ISF
s.Read(isfBytes, 0, (int) s.Length);

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
loadedInk.Load(isfBytes);

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Get the raw data out of this stroke's extended
// properties list, using the previously defined 
// Guid as a key to the extended property.
// Since the save method stored the first and last
// name information as extended properties, this
// information can be remove now that the load is complete.
if (inkProperties.DoesPropertyExist(FirstName))
{
    FirstNameBox.Text = (String) inkProperties[FirstName].Data;
    inkProperties.Remove(FirstName);
}
else
{
    FirstNameBox.Text = String.Empty;
}

if (inkProperties.DoesPropertyExist(LastName))
{
    LastNameBox.Text = (String) inkProperties[LastName].Data;
    inkProperties.Remove(LastName);
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="loading-an-xml-file"></a>Caricamento di un file XML

Il metodo carica un file XML creato in precedenza, recupera i dati dal nodo Ink e converte i dati nel nodo in input penna usando il metodo `LoadXML` Load [dell'oggetto Ink.](/previous-versions/ms569609(v=vs.100)) [](/previous-versions/aa515768(v=msdn.10)) [InkCollector è](/previous-versions/ms836493(v=msdn.10)) temporaneamente disabilitato per assegnare l'oggetto Ink. La casella della firma viene invalidata e le informazioni sul nome e sul cognome vengono recuperate dal documento XML.


```C++
// This object encodes our byte data to a UTF8 string
UTF8Encoding utf8 = new UTF8Encoding();

XmlDocument xd = new XmlDocument();
XmlNodeList nodes;
Ink loadedInk = new Ink();

// Load the XML data into a DOM
xd.Load(s);

// Get the data in the ink node
nodes = xd.GetElementsByTagName("Ink");

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
if (0 != nodes.Count)
    loadedInk.Load(utf8.GetBytes(nodes[0].InnerXml));

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

// Get the data in the FirstName node
nodes = xd.GetElementsByTagName("FirstName");
if (0 != nodes.Count)
{
    FirstNameBox.Text = nodes[0].InnerXml;
}
else
{
    FirstNameBox.Text = String.Empty;
}

// Get the data in the LastName node
nodes = xd.GetElementsByTagName("LastName");
if (0 != nodes.Count)
{
    LastNameBox.Text = nodes[0].InnerXml;
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) form elimina l'oggetto [InkCollector.](/previous-versions/ms836493(v=msdn.10))

 

 
