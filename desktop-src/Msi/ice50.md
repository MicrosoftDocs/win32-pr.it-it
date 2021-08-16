---
description: ICE50 verifica che le icone dei collegamenti vengano visualizzate correttamente e corrispondano all'estensione del file di destinazione.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b9dd81c84c52738ee58c023ba5727cd6d5766bf7c40db97b6459483d7f53d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635152"
---
# <a name="ice50"></a>ICE50

ICE50 verifica che le icone dei collegamenti vengano visualizzate correttamente e corrispondano all'estensione del file di destinazione.

## <a name="result"></a>Risultato

ICE50 invia un messaggio di errore se l'estensione dell'icona e i file di destinazione non corrispondono. ICE50 invia un avviso se le icone vengono archiviate in file che non hanno .exe o con estensione ico.

## <a name="example"></a>Esempio

ICE50 segnala l'errore seguente per l'esempio illustrato.



| Errore o avviso ICE50                                                                                                              | Descrizione                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L'estensione dell'icona 'Icon2.dat' per il collegamento 'Shortcut2' non corrisponde all'estensione del file di chiave per il componente 'Component2'. | Se le estensioni dell'icona e del file di destinazione non corrispondono, il collegamento non avrà il menu di scelta rapida corretto quando il componente viene annunciato. Per correggere l'errore, rinominare l'icona in modo che corrisponda all'estensione del file di destinazione.<br/> |
| L'estensione dell'icona 'Icon1.bat' per il collegamento 'Shortcut1' non è "exe" o "ico". L'icona non verrà visualizzata correttamente.         | Non tutte le versioni della shell visualizzano correttamente le icone archiviate nei file che non hanno estensioni "exe" o "ico". Per correggere questo avviso, rinominare l'icona con estensione "exe" o "ico".<br/>                                      |



 

[Tabella file](file-table.md) (parziale)



| File  | FileName  |
|-------|-----------|
| File1 | File1.bat |
| File2 | File2.pl  |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  |
|----------|
| Funzionalità1 |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | KeyPath |
|------------|---------|
| Componente1 | File1   |
| Componente2 | File2   |



 

[Tabella delle icone](icon-table.md)



| Nome      | Dati            |
|-----------|-----------------|
| Icon1.bat | \[Binary Data\] |
| Icon2.dat | \[Binary Data\] |



 

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente  | Destinazione   | Icona\_    |
|-----------|------------|----------|-----------|
| Collegamento1 | Componente1 | Funzionalità1 | Icon1.bat |
| Collegamento2 | Componente2 | Funzionalità1 | Icon2.dat |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




