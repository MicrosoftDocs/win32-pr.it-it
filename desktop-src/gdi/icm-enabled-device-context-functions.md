---
description: Gestione colori immagini Microsoft (ICM) garantisce che il rendering di un'immagine a colori, un elemento grafico o un oggetto di testo sia il più possibile simile alla finalità originale in qualsiasi dispositivo, nonostante le differenze nelle tecnologie di creazione dell'immagine e nelle funzionalità di colore tra i dispositivi.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled del contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33337aeea32f1ca84b74e3fc45e9bd67dbfe1ce1a5300a502a5303f55cab357
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944201"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled del contesto di dispositivo

Gestione colori immagini Microsoft (ICM) garantisce che il rendering di un'immagine a colori, un elemento grafico o un oggetto di testo sia il più possibile simile alla finalità originale in qualsiasi dispositivo, nonostante le differenze nelle tecnologie di creazione dell'immagine e nelle funzionalità di colore tra i dispositivi. Per altre informazioni, vedere Windows [Color System.](/previous-versions//dd372446(v=vs.85))

Nell'interfaccia GDI (Graphics Device Interface) sono disponibili varie funzioni che usano o operano sui dati di colore. Le funzioni del contesto di dispositivo seguenti sono abilitate per l'uso con ICM:

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
