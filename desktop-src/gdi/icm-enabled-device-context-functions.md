---
description: Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un elemento grafico o un oggetto testo venga sottoposto a rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: Funzioni di contesto del dispositivo ICM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978583"
---
# <a name="icm-enabled-device-context-functions"></a>Funzioni di contesto del dispositivo ICM-Enabled

Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un elemento grafico o un oggetto testo venga sottoposto a rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi. Per ulteriori informazioni, vedere [Windows Color System](/previous-versions//dd372446(v=vs.85)).

Sono disponibili varie funzioni nell'interfaccia GDI (Graphics Device Interface) che usano o operano sui dati di colore. Le funzioni di contesto del dispositivo seguenti sono abilitate per l'uso con ICM:

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
