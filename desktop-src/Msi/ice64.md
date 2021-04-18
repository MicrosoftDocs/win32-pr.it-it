---
description: ICE64 verifica che le nuove directory nel profilo utente vengano rimosse correttamente negli scenari di roaming.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529586"
---
# <a name="ice64"></a>ICE64

ICE64 verifica che le nuove directory nel profilo utente vengano rimosse correttamente negli scenari di roaming.

Se non si corregge un avviso o un errore segnalato da ICE64, in genere si verificano problemi nella pulizia completa del computer durante una disinstallazione. Quando un utente comune che ha installato l'applicazione accede a un computer per la prima volta, tutto il profilo viene copiato nel computer. Nell'annuncio (che si verifica dopo il download del profilo mobile), il programma di installazione verifica che la directory sia già presente e pertanto non la Elimina durante la disinstallazione. Questa operazione lascia la directory nel computer dell'utente in modo permanente.

## <a name="result"></a>Risultato

ICE64 Invia un avviso o un errore in una situazione di roaming se una nuova directory nel profilo utente da rimuovere non viene rimossa.

## <a name="example"></a>Esempio

ICE64 segnala l'errore seguente per l'esempio illustrato.

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

La cartella ' MyOtherFolder ' è una cartella del profilo personalizzata. Poiché non è elencato nella tabella RemoveFile, non viene rimosso in alcuni scenari.

Per correggere l'errore, creare una riga per la cartella nella tabella RemoveFile.

[Tabella directory](directory-table.md)



| Directory     | \_Padre directory | DefaultDir  |
|---------------|-------------------|-------------|
| CartellaDatiApp | TARGETDIR         |             |
| MyFolder      | CartellaDatiApp     | DataFolder  |
| MyOtherFolder | CartellaDatiApp     | DataFolder2 |



 

[Tabella RemoveFile](removefile-table.md)



| FileKey | Componente\_ | FileName | DirProperty | InstallMode |
|---------|-------------|----------|-------------|-------------|
| Chiave1    | Component1  |          | MyFolder    | 2           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



