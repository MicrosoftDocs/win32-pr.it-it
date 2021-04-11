---
description: Questo argomento descrive come compilare un esperto generico fornito con l'SDK Network Monitor.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Creazione di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227386"
---
# <a name="building-an-expert"></a>Creazione di un esperto

Questo argomento descrive come compilare un esperto generico fornito con l'SDK Network Monitor.

> [!Note]  
> Prima di creare gli esempi di codice seguenti, installare il Network Monitor SDK e inizializzare il file di MySetEnv.bat.

 

**Per creare un esperto generico**

1.  Aprire un prompt dei comandi di Network Monitor e passare alla \\ sottodirectory Experts, ad esempio C: \\ Program Files \\ NetMonSDK2 \\ Experts.
2.  Digitare **xcopy/e/s/V Blrplate esperto**; quindi, quando richiesto, digitare **D**.
3.  Passare alla \\ sottodirectory di esperti.
4.  Digitare **Ren Blrplate \* . \* Esperto \* . \***. Verificare che tutti i file siano stati rinominati correttamente. Verificare i nomi dei file confrontando i file nella \\ \\ sottodirectory Experts Blrplate.
5.  Modificare il makefile sostituendo tutte le occorrenze di **Blrplate** con l' **esperto**.
6.  Modificare entrambi i file con estensione cpp sostituendo tutte le occorrenze di **Blrplate** con l' **esperto**. Tenere presente che l'identificatore della finestra di dialogo in config. cpp deve essere in lettere maiuscole (ad esempio, **esperto**).
7.  Modificare il sottoexpert. h sostituendo tutte le occorrenze di **Blrplate** con l' **esperto**.
8.  Modificare Resrc1. h rinominando **BLRPLATE** in **esperto**. (Tenere presente che l' **esperto** deve essere in lettere maiuscole).
9.  Modificare il file con estensione RC di esperti rinominando la **finestra di dialogo di configurazione di IDD \_ BLRPLATE \_ \_** nella **finestra di \_ \_ \_ dialogo di configurazione IDD**.
10. Digitare **NMAKE** per compilare il file dll. Per verificare la compilazione, modificare la directory della \\ sottodirectory obj e verificare che il file esista. Per ulteriori informazioni, vedere [visualizzazione delle proprietà](viewing-expert-dll-properties.md)di una DLL di esperti.

Al termine della compilazione, sarà presente una DLL di esperti che è possibile testare e distribuire con Network Monitor. Per ulteriori informazioni sull'installazione di un esperto, vedere [installazione di un esperto in Network Monitor 2,1](installing-an-expert-to-network-monitor-2-1.md). Per ulteriori informazioni sul debug di un esperto, vedere [debug di un esperto](debugging-an-expert.md).

 

 



