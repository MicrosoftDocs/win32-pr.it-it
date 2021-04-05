---
title: Compilazione del markup della barra multifunzione
description: Affinché il Framework della barra multifunzione di Windows utilizzi il file di markup della barra multifunzione, il file di markup deve essere compilato in un file di risorse in formato binario.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Barra multifunzione di Windows, compilazione del markup
- Barra multifunzione, compilazione del markup
- Barra multifunzione di Windows, flusso di lavoro del compilatore
- Barra multifunzione, flusso di lavoro del compilatore
- Barra multifunzione di Windows, compilatore comando interfaccia utente (UICC.exe)
- Barra multifunzione, compilatore comando interfaccia utente (UICC.exe)
- Compilatore comando interfaccia utente (UICC.exe)
- UICC.exe (compilatore di comandi dell'interfaccia utente)
- compilazione del markup della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515949"
---
# <a name="compiling-ribbon-markup"></a>Compilazione del markup della barra multifunzione

Affinché il Framework della barra multifunzione di Windows utilizzi il file di [markup della barra multifunzione](windowsribbon-schema.md) , il file di markup deve essere compilato in un file di risorse in formato binario. Un compilatore di markup dedicato, il compilatore di comandi dell'interfaccia utente (UICC), è incluso in Windows Software Development Kit (SDK) (7,0 o versione successiva) a questo scopo. Oltre a compilare la versione binaria del markup, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse di tipo immagine e stringa all'applicazione host in fase di compilazione.

-   [Flusso di lavoro del compilatore](#compiler-workflow)
-   [Sintassi della riga di comando](#command-line-syntax)
    -   [Argomenti e opzioni](#arguments-and-options)
    -   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="compiler-workflow"></a>Flusso di lavoro del compilatore

Nel diagramma seguente viene illustrato il flusso di lavoro del compilatore di markup della barra multifunzione.

![diagramma che illustra il flusso di lavoro del compilatore di markup Ribbon.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Sintassi della riga di comando

Nell'esempio seguente viene illustrata la sintassi della riga di comando per il compilatore di markup della barra multifunzione.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Argomenti e opzioni

Gli argomenti e le opzioni per questo strumento sono descritti nella tabella seguente.

> [!Note]  
> Le opzioni della riga di comando elencate devono essere specificate nell'ordine indicato.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/header<headerFile></td>
<td>Genera un file di intestazione denominato <headerFile> che contiene i simboli delle risorse dell'ID comando di markup. Se omesso, non viene generato un file di intestazione.</td>
</tr>
<tr class="even">
<td>/res<resourceFile></td>
<td>Generare un file di risorse denominato <resourceFile> che collega tutte le risorse di tipo image e String, il file di markup binario e il file di intestazione all'applicazione host in fase di compilazione. Se omesso, non viene generato un file di risorse.</td>
</tr>
<tr class="odd">
<td>/Name<ribbonName></td>
<td>Nome della risorsa per il file di markup binario registrato in <resourceFile> . Il valore predefinito è APPLICATION_RIBBON.</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>Filtrare i messaggi di evento in base alla gravità. 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>Solo messaggi di errore.<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>Solo messaggi di errore e di avviso.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Valore predefinito. <br/> Messaggi di errore, di avviso e informativi.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare il compilatore di markup della barra multifunzione per generare un set tipico di file di risorse per un'applicazione Ribbon.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](windowsribbon-schema.md)
</dt> <dt>

[Creazione di un'applicazione Ribbon](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





