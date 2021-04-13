---
description: Prima che le funzioni di installazione possano accedere alle informazioni nel file INF, è necessario aprirlo con una chiamata alla funzione SetupOpenInfFile. Questa funzione restituisce un handle per il file INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Apertura e chiusura di un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529323"
---
# <a name="opening-and-closing-an-inf-file"></a>Apertura e chiusura di un file INF

Prima che le funzioni di installazione possano accedere alle informazioni nel file INF, è necessario aprirlo con una chiamata alla funzione [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) . Questa funzione restituisce un handle per il file INF.

Se non si conosce il nome del file INF che è necessario aprire, è possibile utilizzare la funzione [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) per ottenere un elenco di file inf in una directory.

Dopo aver aperto un file INF, è possibile aggiungere altri file INF al file INF aperto utilizzando la funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) . Il funzionamento è simile a quello di un'istruzione di inclusione. Quando le funzioni di installazione successive fanno riferimento a un file INF aperto, saranno anche in grado di accedere a tutte le informazioni archiviate nei file accodati.

Se non si specifica un file INF durante la chiamata alla funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **SetupOpenAppendInfFile** aggiunge i file specificati dalla chiave **LayoutFile** nella sezione **Version** del file inf aperto.

Quando non sono più necessarie le informazioni nel file INF, chiamare la funzione [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) per rilasciare le risorse allocate durante la chiamata a [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



