---
description: Questa tabella contiene i file di icona. Ogni icona della tabella viene copiata in un file come parte dell'annuncio del prodotto da utilizzare per i collegamenti annunciati e i server OLE. Vedere limitazioni OLE sui flussi.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Icona tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227195"
---
# <a name="icon-table"></a>Icona tabella

Questa tabella contiene i file di icona. Ogni icona della tabella viene copiata in un file come parte dell'annuncio del prodotto da utilizzare per i collegamenti annunciati e i server OLE. Vedere [limitazioni OLE sui flussi](ole-limitations-on-streams.md).

La tabella Icon contiene le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| Nome   | [Identificatore](identifier.md) | S   | N        |
| Data   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome del file icona.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati dell'icona binaria in formato PE (. dll o. exe) o icona (. ico).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene definita quando viene eseguita l' [azione PublishProduct](publishproduct-action.md) .

Le icone per i collegamenti, le estensioni dei nomi di file e i CLSID devono essere archiviati in file separati dal file di destinazione. Questa operazione è necessaria perché il programma di installazione deve copiare solo i file dell'icona piccola nel computer dell'utente quando si annuncia la risorsa. Uno sviluppatore di un pacchetto di installazione deve quindi creare file distinti contenenti solo le icone. Questi file di icona vengono quindi archiviati come dati binari nella tabella delle icone.

I file di icona associati esclusivamente a estensioni di file o CLSID possono avere qualsiasi estensione, ad esempio. ico. Tuttavia, i file di icona associati ai collegamenti devono essere nel formato binario EXE e devono essere denominati in modo tale che l'estensione corrisponda all'estensione della destinazione. Il collegamento non funzionerà se questa regola non è seguita. Se, ad esempio, un collegamento consiste nel puntare a una risorsa con il file di chiave Red.bar, anche il file dell'icona deve avere la barra di estensione. È possibile inserire più icone nello stesso file icona purché tutti i file di destinazione abbiano la stessa estensione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



