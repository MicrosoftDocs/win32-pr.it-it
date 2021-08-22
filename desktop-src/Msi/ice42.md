---
description: ICE42 verifica che i server InProc non siano collegati ai file EXE nella tabella Class. Convalida inoltre che solo le classi LocalServer e LocalServer32 hanno argomenti e valori DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b913b92d82ad25a9722b289596f6b51940bbade55b5e544ebf636051e21b3ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581071"
---
# <a name="ice42"></a>ICE42

ICE42 verifica che i server InProc non siano collegati ai file EXE nella [tabella Class](class-table.md). Convalida inoltre che solo le classi LocalServer e LocalServer32 hanno argomenti e valori DefInProc.

## <a name="result"></a>Risultato

ICE42 invia un errore se sono presenti server InProc collegati ai file EXE nella tabella Class.

## <a name="example"></a>Esempio

ICE42 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE42                                                                                                                             | Descrizione                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IL CLSID '{GUID1}' è un server InProc, ma il componente di implementazione 'Component1' ha un file EXE ('test.exe') come KeyFile.                | È presente un file eseguibile specificato come server InProc. I file EXE non possono essere server InProc.                                                                                                                            |
| Il CLSID '{GUID1}' nel contesto 'InProcServer32' ha un argomento. Solo i contesti LocalServer possono avere argomenti.                              | Per correggere l'errore, rimuovere l'argomento .                                                                                                                                                                                   |
| CLSID '{GUID1}' nel contesto 'InProcServer32' specifica un valore InProc predefinito. Solo i contesti LocalServer possono avere valori InProc predefiniti. | Esiste un oggetto con un valore InProc predefinito che non è un oggetto che opera nei contesti LocalServer o LocalServer32. Per correggere l'errore, rimuovere il valore DeflnProc o modificare il contesto della classe.<br/> |



 

[Tabella di classi](class-table.md) (parziale)



| CLSID   | Context        | Componente\_ | DefInProcHandler | Argomento |
|---------|----------------|-------------|------------------|----------|
| {GUID1} | InProcServer32 | Componente1  | InProcServer     | Arg      |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | KeyPath |
|------------|---------|
| Componente1 | File1   |



 

[Tabella file](file-table.md) (parziale)



| File  | Nome file |
|-------|----------|
| File1 | test.exe |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




