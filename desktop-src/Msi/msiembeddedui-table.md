---
description: La tabella MsiEmbeddedUI definisce un'interfaccia utente incorporata nel pacchetto di Windows Installer.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: Tabella MsiEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52846e88e2d8f3edb439aa6b4a49c99e252173f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321119"
---
# <a name="msiembeddedui-table"></a>Tabella MsiEmbeddedUI

La tabella MsiEmbeddedUI definisce un'interfaccia utente incorporata nel pacchetto di Windows Installer.

**[Windows Installer 4,0 o versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Questa tabella è disponibile a partire da Windows Installer 4,5.

La tabella MsiEmbeddedUI include le colonne seguenti.



| Colonna        | Tipo                               | Chiave | Nullable |
|---------------|------------------------------------|-----|----------|
| MsiEmbeddedUI | [Identificatore](identifier.md)       | S   | N        |
| FileName      | [Text](text.md)                   | N   | N        |
| Attributi    | [Integer](integer.md)             | N   | N        |
| MessageFilter | [DoubleInteger](doubleinteger.md) | N   | S        |
| Data          | [Binario](binary.md)               | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>MsiEmbeddedUI
</dt> <dd>

Chiave primaria per la tabella.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName
</dt> <dd>

Nome del file che riceve le informazioni binarie nella colonna di dati. Il nome del file è obbligatorio per includere un'estensione. Ad esempio, il nome *embeddedui.dll* è accettabile, ma *embeddedui* è inaccettabile. Il nome può essere localizzato. Questo campo può contenere un nome di file breve o un nome di file lungo, ma non può contenere entrambi. Il formato di questo campo è analogo al tipo di dati della colonna [filename](filename.md) , tranne per il fatto che il separatore della barra verticale ( \| ) per la sintassi del nome file breve/nome file lungo non è disponibile. Poiché alcuni server Web possono fare distinzione tra maiuscole e minuscole, il nome file deve corrispondere esattamente al caso dei file di origine per garantire il supporto dei download in Internet.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Informazioni sui dati nella colonna di dati. Il valore in questo campo può contenere una o più delle seguenti costanti.



| Costante                      | Valore esadecimale | Decimal | Significato                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nessuno                          | 0x00        | 0       | Il file non è il file DLL per l'interfaccia utente. Potrebbe trattarsi di un file di risorse utilizzato dall'interfaccia utente.                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | File DLL primario per l'interfaccia utente. Non è possibile contrassegnare più di una riga nella tabella con questo attributo. Se più righe sono contrassegnate con questo attributo, si tratta di un errore e non è possibile garantire quale DLL viene utilizzata. |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | Consente al programma di installazione di richiamare l'interfaccia utente incorporata durante un'installazione a livello di interfaccia utente di base. Questo attributo viene ignorato dal programma di installazione se non è combinato con l'attributo **msidbEmbeddedUI** .                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>MessageFilter
</dt> <dd>

Specifica i tipi di messaggi inviati alla DLL dell'interfaccia utente. Questa colonna è pertinente solo per le righe con l'attributo **msidbEmbeddedUI** . Questo campo deve essere null se una riga fa riferimento a un file di risorse e il valore di Attributes è null. Se una riga fa riferimento a una DLL dell'interfaccia utente, il valore in questa colonna non deve essere null.

Il valore in questa colonna può essere una combinazione dei valori seguenti. Il programma di installazione ignora tutti gli altri valori.



| Costante                           | Valore esadecimale | Decimal   | Descrizione                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **\_FATALEXIT INSTALLLOGMODE**      | 0x00001     | 1         | Terminazione prematura.                                                                                       |
| **\_errore INSTALLLOGMODE**          | 0x00002     | 2         | Messaggi di errore.                                                                                              |
| **avviso di INSTALLLOGMODE \_**        | 0x00004     | 4         | Messaggi di avviso.                                                                                            |
| **\_utente INSTALLLOGMODE**           | 0x00008     | 8         | Messaggi utente.                                                                                               |
| **\_informazioni INSTALLLOGMODE**           | 0x00010     | 16        | Messaggi di stato non registrati.                                                                                    |
| **filesinus INSTALLLOGMODE \_**     | 0x00020     | 32        | File attualmente in uso.                                                                                 |
| **\_RESOLVESOURCE INSTALLLOGMODE**  | 0x00040     | 64        | Richieste di risoluzione dell'origine.                                                                                  |
| **\_OUTOFDISKSPACE INSTALLLOGMODE** | 0x00080     | 128       | Messaggi di spazio su disco.                                                                                         |
| **\_ACTIONSTART INSTALLLOGMODE**    | 0x00100     | 256       | Messaggi di avvio dell'azione.                                                                                       |
| **\_ACTIONDATA INSTALLLOGMODE**     | 0x00200     | 512       | Messaggi dati azione.                                                                                        |
| **\_stato INSTALLLOGMODE**       | 0x00400     | 1024      | Messaggi di stato.                                                                                           |
| **\_COMMONDATA INSTALLLOGMODE**     | 0x00800     | 2048      | Messaggi di inizializzazione dell'interfaccia utente.                                                                                  |
| **\_inizializzazione INSTALLLOGMODE**     | 0x01000     | 4096      | Messaggi di avvio dell'interfaccia utente inviati al momento dell'avvio dell'installazione di un prodotto.                                            |
| **\_terminazione INSTALLLOGMODE**      | 0x02000     | 8192      | Messaggi di chiusura dell'interfaccia utente inviati al termine di un'installazione del prodotto.                                         |
| **INSTALLLOGMODE \_ SHOWDIALOG**     | 0x04000     | 16384     | Messaggi inviati prima della visualizzazione della finestra di dialogo dell'interfaccia utente.                                                             |
| **\_RMFILESINUSE INSTALLLOGMODE**   | 0x02000000  | 33554432  | File attualmente in uso.                                                                                 |
| **\_INSTALLSTART INSTALLLOGMODE**   | 0x04000000  | 67108864  | Viene avviata l'installazione del prodotto. Il messaggio contiene il ProductName e ProductCode del prodotto.              |
| **\_INSTALLEND INSTALLLOGMODE**     | 0x08000000  | 134217728 | L'installazione del prodotto termina. Il messaggio contiene il valore ProductName, ProductCode e il valore restituito del prodotto. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Questa colonna contiene informazioni binarie. Se il campo attributo è contrassegnato con l'attributo **msidbEmbeddedUI** , le informazioni contenute in questo campo devono essere una dll. Se il campo attributo non è l'attributo **msidbEmbeddedUI** , le informazioni contenute in questo campo possono essere un file di risorse in qualsiasi formato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare un'interfaccia utente incorporata, lo sviluppatore del programma di installazione deve creare questa funzionalità nel pacchetto di Windows Installer. La tabella MsiEmbeddedUI definisce l'interfaccia utente incorporata. La DLL per l'interfaccia utente incorporata deve esportare le funzioni *InitializeEmbeddedUI*, *EmbeddedUIHandler* e *ShutdownEmbeddedUI* . I pacchetti che non supportano un'interfaccia utente incorporata possono utilizzare l'interfaccia utente Windows Installer interna.

Per eseguire [gli strumenti di debug per Windows](https://www.microsoft.com/?ref=go) in un'interfaccia utente incorporata, usare le tecniche descritte in [debug delle azioni personalizzate](debugging-custom-actions.md). Impostare il valore di MsiBreak su MsiEmbeddedUI.

Per un esempio di un'interfaccia utente personalizzata incorporata, vedere [uso di un'interfaccia utente incorporata](using-an-embedded-ui.md).

 

 



