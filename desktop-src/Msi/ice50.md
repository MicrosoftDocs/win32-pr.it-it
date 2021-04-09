---
description: ICE50 verifica che le icone di collegamento vengano specificate per la visualizzazione corretta e corrispondano all'estensione del file di destinazione.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968100"
---
# <a name="ice50"></a>ICE50

ICE50 verifica che le icone di collegamento vengano specificate per la visualizzazione corretta e corrispondano all'estensione del file di destinazione.

## <a name="result"></a>Risultato

ICE50 Invia un messaggio di errore se l'estensione dei file di icona e di destinazione non corrisponde. ICE50 pubblica un avviso se le icone sono archiviate in file che non hanno un'estensione. exe o. ico.

## <a name="example"></a>Esempio

ICE50 segnala l'errore seguente per l'esempio illustrato.



| Errore o avviso ICE50                                                                                                              | Descrizione                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L'estensione dell'icona ' icon2. dat ' per il collegamento ' Shortcut2' non corrisponde all'estensione del file di chiave per il componente ' Component2'. | Se le estensioni dell'icona e il file di destinazione non corrispondono, il collegamento non avrà il menu di scelta rapida corretto quando viene annunciato il componente. Per correggere l'errore, rinominare l'icona in modo che corrisponda all'estensione del file di destinazione.<br/> |
| L'estensione dell'icona ' Icon1.bat' per il collegamento ' Shortcut1' non è "exe" o "ico". L'icona non viene visualizzata correttamente.         | Non tutte le versioni della shell visualizzano correttamente le icone archiviate in file privi di estensioni di "exe" o "ico". Per correggere il problema, rinominare l'icona con estensione "exe" o "ico".<br/>                                      |



 

[Tabella file](file-table.md) (parziale)



| File  | FileName  |
|-------|-----------|
| File1 | File1.bat |
| File2 | File2.pl  |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  |
|----------|
| Feature1 |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | KeyPath |
|------------|---------|
| Component1 | File1   |
| Component2 | File2   |



 

[Icona tabella](icon-table.md)



| Nome      | Data            |
|-----------|-----------------|
| Icon1.bat | \[Binary Data\] |
| Icon2. dat | \[Binary Data\] |



 

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente  | Destinazione   | Icona\_    |
|-----------|------------|----------|-----------|
| Shortcut1 | Component1 | Feature1 | Icon1.bat |
| Shortcut2 | Component2 | Feature1 | Icon2. dat |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




