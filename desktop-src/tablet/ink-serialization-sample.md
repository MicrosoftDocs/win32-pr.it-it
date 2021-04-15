---
description: In questo esempio viene illustrato come serializzare e deserializzare l'input penna in vari formati.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Esempio di serializzazione dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e898f91db17efcb7579c067e7db5c422da8213a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525290"
---
# <a name="ink-serialization-sample"></a><span data-ttu-id="1959d-103">Esempio di serializzazione dell'input penna</span><span class="sxs-lookup"><span data-stu-id="1959d-103">Ink Serialization Sample</span></span>

<span data-ttu-id="1959d-104">In questo esempio viene illustrato come serializzare e deserializzare l'input penna in vari formati.</span><span class="sxs-lookup"><span data-stu-id="1959d-104">This sample demonstrates how to serialize and de-serialize ink in various formats.</span></span> <span data-ttu-id="1959d-105">L'applicazione rappresenta un modulo con campi per inserire nome, cognome e firma.</span><span class="sxs-lookup"><span data-stu-id="1959d-105">The application represents a form with fields for inputting first name, last name, and signature.</span></span> <span data-ttu-id="1959d-106">L'utente può salvare questi dati sotto forma di formato ISF (pure Ink Serialized Format), Extensible Markup Language (XML) usando l'ISF con codifica Base64 o HTML, che fa riferimento a input penna in un'immagine di Graphics Interchange Format con codifica Base64 (GIF).</span><span class="sxs-lookup"><span data-stu-id="1959d-106">The user may save this data as pure ink serialized format (ISF), Extensible Markup Language (XML) using base64 encoded ISF, or HTML, which references ink in a base64 encoded fortified Graphics Interchange Format (GIF) image.</span></span> <span data-ttu-id="1959d-107">L'applicazione consente inoltre all'utente di aprire i file salvati come formati XML e ISF.</span><span class="sxs-lookup"><span data-stu-id="1959d-107">The application also enables the user to open files that were saved as XML and ISF formats.</span></span> <span data-ttu-id="1959d-108">Il formato ISF usa le proprietà estese per archiviare il nome e il cognome, mentre i formati XML e HTML archiviano queste informazioni negli attributi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1959d-108">The ISF format uses extended properties to store the first name and last name, whereas the XML and HTML formats store this information in custom attributes.</span></span>

<span data-ttu-id="1959d-109">Questo esempio non supporta il caricamento dal formato HTML, perché HTML non è adatto per l'archiviazione di dati strutturati.</span><span class="sxs-lookup"><span data-stu-id="1959d-109">This sample does not support loading from the HTML format, because HTML is not suitable for storing structured data.</span></span> <span data-ttu-id="1959d-110">Poiché i dati sono separati in nome, firma e così via, è necessario un formato che conserva questa separazione, ad esempio XML o un altro tipo di formato di database.</span><span class="sxs-lookup"><span data-stu-id="1959d-110">Because the data is separated into name, signature, and so on, a format that preserves this separation, such as XML or another kind of database format, is required.</span></span>

<span data-ttu-id="1959d-111">HTML è molto utile in un ambiente in cui la formattazione è importante, ad esempio in un documento di elaborazione di testo.</span><span class="sxs-lookup"><span data-stu-id="1959d-111">HTML is very useful in an environment in which formatting is important, such as in a word processing document.</span></span> <span data-ttu-id="1959d-112">Il codice HTML salvato da questo esempio usa le gif fortificate.</span><span class="sxs-lookup"><span data-stu-id="1959d-112">The HTML that is saved by this sample uses fortified GIFs.</span></span> <span data-ttu-id="1959d-113">Queste gif hanno incorporate ISF, in modo da mantenere la fedeltà completa dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="1959d-113">These GIFs have ISF embedded within them, which preserves the full fidelity of the ink.</span></span> <span data-ttu-id="1959d-114">Un'applicazione di elaborazione di testo può salvare un documento contenente più tipi di dati, ad esempio immagini, tabelle, testo formattato e input penna salvati in un formato HTML.</span><span class="sxs-lookup"><span data-stu-id="1959d-114">A word processing application can save a document containing multiple types of data, such as images, tables, formatted text, and ink persisted in an HTML format.</span></span> <span data-ttu-id="1959d-115">Il rendering del codice HTML viene eseguito nei browser che non riconoscono l'input penna.</span><span class="sxs-lookup"><span data-stu-id="1959d-115">This HTML would render in browsers that do not recognize ink.</span></span> <span data-ttu-id="1959d-116">Tuttavia, quando viene caricato in un'applicazione abilitata per l'input penna, la fedeltà completa dell'input penna originale è disponibile e può essere sottoposta a rendering, modificata o utilizzata per il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="1959d-116">However, when loaded into an application that is ink-enabled, the full fidelity of the original ink is available and can be rendered, edited, or used for recognition.</span></span>

<span data-ttu-id="1959d-117">In questo esempio vengono usate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="1959d-117">The following features are used in this sample:</span></span>

-   <span data-ttu-id="1959d-118">Metodo [Load](/previous-versions/ms569609(v=vs.100)) dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1959d-118">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method</span></span>
-   <span data-ttu-id="1959d-119">Metodo [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1959d-119">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method</span></span>
-   <span data-ttu-id="1959d-120">Proprietà [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1959d-120">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property</span></span>

## <a name="collecting-ink"></a><span data-ttu-id="1959d-121">Raccolta di input penna</span><span class="sxs-lookup"><span data-stu-id="1959d-121">Collecting Ink</span></span>

<span data-ttu-id="1959d-122">Per prima cosa, fare riferimento all'API Tablet PC installata con Windows Vista e Windows XP Tablet PC Edition Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1959d-122">First, reference the Tablet PC API, which are installed with the Windows Vista and Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="1959d-123">Il costruttore crea e Abilita un oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , per il form.</span><span class="sxs-lookup"><span data-stu-id="1959d-123">The constructor creates and enables an [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic`, for the form.</span></span>


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a><span data-ttu-id="1959d-124">Salvataggio di un file</span><span class="sxs-lookup"><span data-stu-id="1959d-124">Saving a File</span></span>

<span data-ttu-id="1959d-125">Il `SaveAsMenu_Click` metodo gestisce la finestra di dialogo Salva con nome, crea un flusso di file in cui salvare i dati di input penna e chiama il metodo Save che corrisponde alla scelta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1959d-125">The `SaveAsMenu_Click` method handles the Save As dialog box, creates a file stream in which to save the ink data, and calls the save method that corresponds to the user's choice.</span></span>

## <a name="saving-to-an-isf-file"></a><span data-ttu-id="1959d-126">Salvataggio in un file ISF</span><span class="sxs-lookup"><span data-stu-id="1959d-126">Saving to an ISF File</span></span>

<span data-ttu-id="1959d-127">Nel `SaveISF` metodo, i valori First e Last Name vengono aggiunti alla proprietà [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) della proprietà [Ink](/previous-versions/ms836505(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , prima che l'input penna venga serializzato e scritto nel file.</span><span class="sxs-lookup"><span data-stu-id="1959d-127">In the `SaveISF` method, the first and last name values are added to the [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property of the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [Ink](/previous-versions/ms836505(v=msdn.10)) property, before the ink is serialized and written to the file.</span></span> <span data-ttu-id="1959d-128">Dopo che l'input penna è stato serializzato, i valori del nome e del cognome vengono rimossi dalla proprietà ExtendedProperties dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1959d-128">After the ink has been serialized, the first and last name values are removed from the [Ink](/previous-versions/aa515768(v=msdn.10)) object's ExtendedProperties property.</span></span>


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



## <a name="saving-to-an-xml-file"></a><span data-ttu-id="1959d-129">Salvataggio in un file XML</span><span class="sxs-lookup"><span data-stu-id="1959d-129">Saving to an XML File</span></span>

<span data-ttu-id="1959d-130">Nel `SaveXML` metodo viene utilizzato un oggetto [XmlWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) per creare e scrivere in un documento XML.</span><span class="sxs-lookup"><span data-stu-id="1959d-130">In the `SaveXML` method, an [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) object is used to create and write to an XML document.</span></span> <span data-ttu-id="1959d-131">Utilizzando il metodo [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) , l'input penna viene prima convertito in una matrice di byte in formato serializzato con input penna Base64, quindi la matrice di byte viene convertita in una stringa da scrivere nel file XML.</span><span class="sxs-lookup"><span data-stu-id="1959d-131">Using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, the ink is first converted to a base64 encoded Ink Serialized Format byte array, and then the byte array is converted to a string to be written out to the XML file.</span></span> <span data-ttu-id="1959d-132">Anche i dati di testo del modulo vengono scritti nel file XML.</span><span class="sxs-lookup"><span data-stu-id="1959d-132">The text data from the form is also written out to the XML file.</span></span>


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



## <a name="saving-to-an-html-file"></a><span data-ttu-id="1959d-133">Salvataggio in un file HTML</span><span class="sxs-lookup"><span data-stu-id="1959d-133">Saving to an HTML File</span></span>

<span data-ttu-id="1959d-134">Il metodo SaveHTML usa il rettangolo di delimitazione della raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) per verificare la presenza di una firma.</span><span class="sxs-lookup"><span data-stu-id="1959d-134">The SaveHTML method uses the bounding box of the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection to test for the presence of a signature.</span></span> <span data-ttu-id="1959d-135">Se la firma esiste, viene convertita nel formato GIF fortificato usando il metodo [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto Ink e scritta in un file.</span><span class="sxs-lookup"><span data-stu-id="1959d-135">If the signature exists, it is converted to the fortified GIF format using the ink object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, and written to a file.</span></span> <span data-ttu-id="1959d-136">Al GIF viene quindi fatto riferimento nel file HTML.</span><span class="sxs-lookup"><span data-stu-id="1959d-136">The GIF is then referenced in the HTML file.</span></span>


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



## <a name="loading-a-file"></a><span data-ttu-id="1959d-137">Caricamento di un file</span><span class="sxs-lookup"><span data-stu-id="1959d-137">Loading a File</span></span>

<span data-ttu-id="1959d-138">Il `OpenMenu_Click` metodo gestisce la finestra di dialogo Apri, apre il file e chiama il metodo di caricamento che corrisponde alla scelta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1959d-138">The `OpenMenu_Click` method handles the Open dialog box, opens the file, and calls the loading method that corresponds to the user's choice.</span></span>

## <a name="loading-an-isf-file"></a><span data-ttu-id="1959d-139">Caricamento di un file ISF</span><span class="sxs-lookup"><span data-stu-id="1959d-139">Loading an ISF File</span></span>

<span data-ttu-id="1959d-140">Il `LoadISF` metodo legge il file creato in precedenza e converte la matrice di byte in input penna con il metodo [Load](/previous-versions/ms569609(v=vs.100)) dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1959d-140">The `LoadISF` method reads the previously created file and converts the Byte array to ink with the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="1959d-141">L'agente di raccolta input penna è temporaneamente disabilitato per assegnare l'oggetto Ink.</span><span class="sxs-lookup"><span data-stu-id="1959d-141">The ink collector is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="1959d-142">Il `LoadISF` metodo verifica quindi la proprietà [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) dell'oggetto Ink per le stringhe First e Last Name.</span><span class="sxs-lookup"><span data-stu-id="1959d-142">The `LoadISF` method then checks the Ink object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property for the first and last name strings.</span></span>


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



## <a name="loading-an-xml-file"></a><span data-ttu-id="1959d-143">Caricamento di un file XML</span><span class="sxs-lookup"><span data-stu-id="1959d-143">Loading an XML File</span></span>

<span data-ttu-id="1959d-144">`LoadXML`Tramite il metodo viene caricato un file XML creato in precedenza, vengono recuperati i dati dal nodo Ink e i dati del nodo vengono convertiti in input penna utilizzando il metodo [Load](/previous-versions/ms569609(v=vs.100)) dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1959d-144">The `LoadXML` method loads a previously created XML file, retrieves data from the Ink node, and converts the data in the node to ink using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="1959d-145">Il [InkCollector](/previous-versions/ms836493(v=msdn.10)) è temporaneamente disabilitato per assegnare l'oggetto Ink.</span><span class="sxs-lookup"><span data-stu-id="1959d-145">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="1959d-146">La casella firma viene invalidata e le informazioni relative al nome e al cognome vengono recuperate dal documento XML.</span><span class="sxs-lookup"><span data-stu-id="1959d-146">The signature box is invalidated, and the first and last name information is retrieved from the XML document.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="1959d-147">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="1959d-147">Closing the Form</span></span>

<span data-ttu-id="1959d-148">Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1959d-148">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object.</span></span>

 

 
