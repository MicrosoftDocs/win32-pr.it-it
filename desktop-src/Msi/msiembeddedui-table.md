---
description: La tabella MsiEmbeddedUI definisce un'interfaccia utente incorporata nel pacchetto Windows Installer.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: Tabella MsiEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7357a0b5aa1de2218eefb58fa85fbe374e9796ad0aaa94946743f1c51d9c8daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012949"
---
# <a name="msiembeddedui-table"></a>Tabella MsiEmbeddedUI

La tabella MsiEmbeddedUI definisce un'interfaccia utente incorporata nel pacchetto Windows Installer.

**[Windows Installer 4.0 o versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato. Questa tabella è disponibile a partire da Windows Installer 4.5.

La tabella MsiEmbeddedUI include le colonne seguenti.



| Colonna        | Tipo                               | Chiave | Nullable |
|---------------|------------------------------------|-----|----------|
| MsiEmbeddedUI | [Identificatore](identifier.md)       | S   | N        |
| FileName      | [Text](text.md)                   | N   | N        |
| Attributi    | [Integer](integer.md)             | N   | N        |
| Messagefilter | [DoubleInteger](doubleinteger.md) | N   | S        |
| Dati          | [Binario](binary.md)               | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>MsiEmbeddedUI
</dt> <dd>

Chiave primaria per la tabella.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Nome del file che riceve le informazioni binarie nella colonna Dati. Il nome del file è necessario per includere un'estensione. Ad esempio, il nome *embeddedui.dll* è accettabile, ma *embeddedui* è inammissibile. Il nome può essere localizzato. Questo campo può contenere un nome di file breve o un nome file lungo, ma non può contenere entrambi. Il formato di questo [](filename.md) campo è simile al tipo di dati Della colonna Nome file, ad eccezione del fatto che il separatore della barra verticale ( ) per la sintassi del nome \| file breve/nome file lungo non è disponibile. Poiché alcuni server Web possono fare distinzione tra maiuscole e minuscole, FileName deve corrispondere esattamente alla distinzione tra maiuscole e minuscole dei file di origine per garantire il supporto dei download Internet.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Informazioni sui dati nella colonna Dati. Il valore in questo campo può contenere una o più delle costanti seguenti.



| Costante                      | Valore esadecimale | Decimal | Significato                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nessuno                          | 0x00        | 0       | Il file non è il file DLL per l'interfaccia utente. Può trattarsi di un file di risorse usato dall'interfaccia utente.                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | File DLL primario per l'interfaccia utente. Non più di una riga nella tabella può essere contrassegnata con questo attributo. Se più righe sono contrassegnate con questo attributo, si tratta di un errore e non è possibile garantire quale DLL viene utilizzata. |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | Consente al programma di installazione di richiamare l'interfaccia utente incorporata durante un'installazione a livello di interfaccia utente di base. Il programma di installazione ignora questo attributo se non viene combinato con **l'attributo msidbEmbeddedUI.**                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>Messagefilter
</dt> <dd>

Specifica i tipi di messaggi inviati alla DLL dell'interfaccia utente. Questa colonna è pertinente solo per le righe con **l'attributo msidbEmbeddedUI.** Questo campo deve essere Null se una riga fa riferimento a un file di risorse e il valore di Attributi è Null. Se una riga fa riferimento a una DLL dell'interfaccia utente, il valore in questa colonna non deve essere Null.

Il valore in questa colonna può essere una combinazione dei valori seguenti. Il programma di installazione ignora qualsiasi altro valore.



| Costante                           | Valore esadecimale | Decimal   | Descrizione                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **INSTALLLOGMODE \_ FATALEXIT**      | 0x00001     | 1         | Terminazione prematura.                                                                                       |
| **ERRORE \_ INSTALLLOGMODE**          | 0x00002     | 2         | Messaggi di errore.                                                                                              |
| **AVVISO \_ INSTALLLOGMODE**        | 0x00004     | 4         | Messaggi di avviso.                                                                                            |
| **UTENTE \_ INSTALLLOGMODE**           | 0x00008     | 8         | Messaggi utente.                                                                                               |
| **INFORMAZIONI SU \_ INSTALLLOGMODE**           | 0x00010     | 16        | Messaggi di stato non scaricati.                                                                                    |
| **FILE \_ INSTALLLOGMODEINUSE**     | 0x00020     | 32        | File attualmente in uso.                                                                                 |
| **INSTALLLOGMODE \_ RESOLVESOURCE**  | 0x00040     | 64        | Richieste di risoluzione dell'origine.                                                                                  |
| **INSTALLLOGMODE \_ OUTOFDISKSPACE** | 0x00080     | 128       | Messaggi relativi allo spazio su disco.                                                                                         |
| **INSTALLLOGMODE \_ ACTIONSTART**    | 0x00100     | 256       | Messaggi di avvio dell'azione.                                                                                       |
| **INSTALLLOGMODE \_ ACTIONDATA**     | 0x00200     | 512       | Messaggi di dati dell'azione.                                                                                        |
| **STATO \_ INSTALLLOGMODE**       | 0x00400     | 1024      | Messaggi di stato.                                                                                           |
| **INSTALLLOGMODE \_ COMMONDATA**     | 0x00800     | 2048      | Messaggi di inizializzazione dell'interfaccia utente.                                                                                  |
| **INSTALLLOGMODE \_ INITIALIZE**     | 0x01000     | 4096      | Messaggi di avvio dell'interfaccia utente inviati all'avvio dell'installazione di un prodotto.                                            |
| **INSTALLLOGMODE \_ TERMINATE**      | 0x02000     | 8192      | Messaggi di arresto dell'interfaccia utente inviati al termine dell'installazione di un prodotto.                                         |
| **INSTALLLOGMODE \_ SHOWDIALOG**     | 0x04000     | 16384     | Messaggi inviati prima della visualizzazione della finestra di dialogo dell'interfaccia utente.                                                             |
| **INSTALLLOGMODE \_ RMFILESINUSE**   | 0x02000000  | 33554432  | File attualmente in uso.                                                                                 |
| **INSTALLLOGMODE \_ INSTALLSTART**   | 0x04000000  | 67108864  | Viene avviata l'installazione del prodotto. Il messaggio contiene productName e ProductCode del prodotto.              |
| **INSTALLLOGMODE \_ INSTALLEND**     | 0x08000000  | 134217728 | L'installazione del prodotto termina. Il messaggio contiene productName, ProductCode e il valore restituito del prodotto. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Questa colonna contiene informazioni binarie. Se il campo Attributo è contrassegnato con **l'attributo msidbEmbeddedUI,** le informazioni in questo campo devono essere una DLL. Se il campo Attributo non è **l'attributo msidbEmbeddedUI,** le informazioni contenute in questo campo possono essere un file di risorse in qualsiasi formato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare un'interfaccia utente incorporata, lo sviluppatore del programma di installazione deve creare questa funzionalità nel pacchetto Windows Installer. La tabella MsiEmbeddedUI definisce l'interfaccia utente incorporata. La DLL per l'interfaccia utente incorporata deve esportare *le funzioni InitializeEmbeddedUI*, *EmbeddedUIHandler* e *ShutdownEmbeddedUI.* I pacchetti che non supportano un'interfaccia utente incorporata possono usare l Windows intervai utente interna del programma di installazione.

Per eseguire [gli strumenti di debug Windows](https://www.microsoft.com/?ref=go) in un'interfaccia utente incorporata, usare le tecniche descritte in Debug di azioni [personalizzate.](debugging-custom-actions.md) Impostare il valore di MsiBreak su MsiEmbeddedUI.

Per un esempio di interfaccia utente personalizzata incorporata, vedere [Uso di un'interfaccia utente incorporata.](using-an-embedded-ui.md)

 

 



