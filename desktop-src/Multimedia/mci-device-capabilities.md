---
title: Funzionalità del dispositivo MCI
description: Funzionalità del dispositivo MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig (macro)
- MCIWndCanEject (macro)
- MCIWndCanPlay (macro)
- MCIWndCanRecord (macro)
- MCIWndCanSave (macro)
- MCIWndCanWindow (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045265"
---
# <a name="mci-device-capabilities"></a>Funzionalità del dispositivo MCI

MCIWnd include le macro seguenti per consentire l'esecuzione di query sui dispositivi MCI per le rispettive funzionalità.



| Macro                                      | Descrizione                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Determina se un dispositivo ha una finestra di dialogo di configurazione per supportare più configurazioni, ad esempio il dispositivo MCIAVI.                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Determina se un dispositivo dispone di una funzione di espulsione controllata dal software.                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Determina se un dispositivo è in grado di riprodurre il contenuto esistente.                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Determina se un dispositivo è in grado di registrare.                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Determina se un dispositivo può archiviare i dati.                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Determina se un dispositivo supporta i comandi della finestra MCI, ad esempio [**finestra**](window.md), [**put**](put.md) e [**where**](where.md). |



 

Queste macro restituiscono **true** se il dispositivo supporta la funzionalità specifica o **false** in caso contrario.

 

 




