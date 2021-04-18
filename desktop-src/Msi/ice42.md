---
description: ICE42 verifica che i server inproc non siano collegati ai file EXE nella tabella della classe. Viene inoltre convalidato che solo le classi LocalServer e LocalServer32 dispongono di argomenti e valori DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314214"
---
# <a name="ice42"></a>ICE42

ICE42 verifica che i server inproc non siano collegati ai file EXE nella [tabella della classe](class-table.md). Viene inoltre convalidato che solo le classi LocalServer e LocalServer32 dispongono di argomenti e valori DefInProc.

## <a name="result"></a>Risultato

ICE42 Invia un errore se sono presenti server inproc collegati ai file EXE nella tabella della classe.

## <a name="example"></a>Esempio

ICE42 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE42                                                                                                                             | Descrizione                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il CLSID ' {GUID1}' è un server inproc, ma il componente di implementazione ' Component1' ha un file con estensione EXE (' test.exe') come file di base.                | È presente un file eseguibile specificato come server inproc. I file EXE non possono essere server inproc.                                                                                                                            |
| Il CLSID ' {GUID1}' nel contesto ' InProcServer32' contiene un argomento. Solo i contesti LocalServer possono avere argomenti.                              | Per correggere l'errore, rimuovere l'argomento.                                                                                                                                                                                   |
| Il CLSID ' {GUID1}' nel contesto ' InProcServer32' specifica un valore InProc predefinito. Solo i contesti LocalServer possono avere valori InProc predefiniti. | È presente un oggetto con un valore InProc predefinito che non è un oggetto che opera nei contesti LocalServer o LocalServer32. Per correggere l'errore, rimuovere il valore DeflnProc o modificare il contesto della classe.<br/> |



 

[Tabella classi](class-table.md) (parziale)



| CLSID   | Context        | Componente\_ | DefInProcHandler | Argomento |
|---------|----------------|-------------|------------------|----------|
| Guid1 | InProcServer32 | Component1  | InProcServer     | ARG      |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | KeyPath |
|------------|---------|
| Component1 | File1   |



 

[Tabella file](file-table.md) (parziale)



| File  | Nome file |
|-------|----------|
| File1 | test.exe |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




