---
description: Questo argomento descrive come creare un esperto generico fornito con Network Monitor SDK.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Creazione di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbffc036f27ad0b91fb19906c5f12740919828b33ebfced584e068abe93bd912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064251"
---
# <a name="building-an-expert"></a>Creazione di un esperto

Questo argomento descrive come creare un esperto generico fornito con Network Monitor SDK.

> [!Note]  
> Prima di creare gli esempi di codice seguenti, installare Network Monitor SDK e inizializzare il file MySetEnv.bat.

 

**Per creare un esperto generico**

1.  Aprire un prompt Network Monitor prompt dei comandi e passare alla sottodirectory Experts, ad esempio \\ C: \\ Programmi \\ NetMonSDK2 \\ Experts.
2.  Digitare **xcopy /e /s /v Blrplate MyExpert**; quindi, quando richiesto, digitare **D**.
3.  Passare alla \\ sottodirectory MyExpert.
4.  Digitare **ren Blrplate \* . \* MyExpert \* \* .** Assicurarsi che tutti i file siano stati rinominati correttamente. Verificare i nomi dei file confrontando i file nella \\ sottodirectory Experts \\ Blrplate.
5.  Modificare il makefile sostituendo tutte le occorrenze di **Blrplate** con **MyExpert.**
6.  Modificare entrambi i file con estensione cpp sostituendo tutte le occorrenze di **Blrplate** con **MyExpert.** Tenere presente che l'identificatore della finestra di dialogo in Config.cpp deve essere in lettere maiuscole (ad esempio, **MYEXPERT).**
7.  Modificare MyExpert.h sostituendo tutte le occorrenze di **Blrplate** con **MyExpert**.
8.  Modificare Resrc1.h rinominando **BLRPLATE** in **MYEXPERT.** Tenere presente che **MYEXPERT** deve essere in lettere maiuscole.
9.  Modificare il file MyExpert.rc rinominando **IDD \_ BLRPLATE \_ CONFIG \_ DIALOG** in **IDD \_ MYEXPERT \_ CONFIG \_ DIALOG**.
10. Digitare **nmake per** compilare il file DLL. Per verificare la compilazione, passare alla \\ sottodirectory Obj e verificare che il file esista. Per altre informazioni, vedere [Visualizzazione delle proprietà della DLL Expert.](viewing-expert-dll-properties.md)

Al termine della compilazione, si avrà una DLL esperta che è possibile testare e distribuire con Network Monitor. Per altre informazioni sull'installazione di un esperto, vedere [Installing an Expert to Network Monitor 2.1 (Installazione di un esperto Network Monitor 2.1).](installing-an-expert-to-network-monitor-2-1.md) Per altre informazioni sul debug di un esperto, vedere [Debug di un esperto.](debugging-an-expert.md)

 

 



