---
description: Prima che le funzioni di installazione possano accedere alle informazioni in INF, è necessario aprirle con una chiamata alla funzione SetupOpenInfFile. Questa funzione restituisce un handle per il file INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Apertura e chiusura di un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05500b473a904a3834fa507cff0d22c466153f4e08d95f75d0c076c66d86675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665551"
---
# <a name="opening-and-closing-an-inf-file"></a>Apertura e chiusura di un file INF

Prima che le funzioni di installazione possano accedere alle informazioni in INF, è necessario aprirle con una chiamata alla [**funzione SetupOpenInfFile.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) Questa funzione restituisce un handle per il file INF.

Se non si conosce il nome del file INF che è necessario aprire, è possibile usare la funzione [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) per ottenere un elenco di file INF in una directory.

Dopo aver aperto un file INF, è possibile aggiungere altri file INF al file INF aperto usando la [**funzione SetupOpenAppendInfFile.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) Dal punto di vista funzionale è simile a un'istruzione include. Quando le funzioni di installazione successive fanno riferimento a un file INF aperto, potranno accedere anche alle informazioni archiviate nei file accodati.

Se non si specifica un file INF durante la chiamata alla funzione [**SetupOpenAppendInfFile,**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) **SetupOpenAppendInfFile** aggiunge i file specificati dalla chiave **LayoutFile** nella sezione **Version** del file INF aperto.

Quando le informazioni nel file INF non sono più necessarie, chiamare la funzione [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) per rilasciare le risorse allocate durante la chiamata a [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



