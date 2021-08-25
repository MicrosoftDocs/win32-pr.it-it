---
description: Le funzioni seguenti vengono usate con i contesti di dispositivo.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Funzioni del contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33eda03ce65a5873c4420f6675128243e30493dc75fa3055c8718f6826f4a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966051"
---
# <a name="device-context-functions"></a>Funzioni del contesto di dispositivo

Le funzioni seguenti vengono usate con i contesti di dispositivo.



| Funzione                                                   | Descrizione                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Annulla qualsiasi operazione in sospeso nel contesto di dispositivo specificato.                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Modifica le impostazioni del dispositivo di visualizzazione predefinito sulla modalità grafica specificata.                                                        |
| [**Changedisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Modifica le impostazioni del dispositivo di visualizzazione specificato nella modalità grafica specificata.                                                      |
| [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Crea un contesto di dispositivo di memoria compatibile con il dispositivo specificato.                                                                     |
| [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Crea un contesto di dispositivo per un dispositivo usando il nome specificato.                                                                           |
| [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Crea un contesto di informazioni per il dispositivo specificato.                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Elimina il contesto di dispositivo specificato.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Elimina una penna, un pennello, un tipo di carattere, una bitmap, un'area o una tavolozza logica, liberando tutte le risorse di sistema associate all'oggetto .                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Recupera le funzionalità di un driver di dispositivo della stampante.                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Fornisce funzionalità di disegno della visualizzazione video specificata che non sono direttamente disponibili tramite l'interfaccia grafica del dispositivo.       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Recupera informazioni sui dispositivi di visualizzazione in un sistema.                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Recupera informazioni su una delle modalità grafiche per un dispositivo di visualizzazione.                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Recupera informazioni su una delle modalità grafiche per un dispositivo di visualizzazione.                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Enumera le penna o i pennelli disponibili per il contesto di dispositivo specificato.                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Funzione di callback definita dall'applicazione usata con la [**funzione EnumObjects.**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                                       |
| [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Recupera un handle per un oggetto del tipo specificato selezionato nel contesto di dispositivo specificato.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Recupera un handle per un contesto di dispositivo di visualizzazione per l'area client di una finestra specificata o per l'intero schermo.                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Recupera il colore del pennello corrente per il contesto di dispositivo specificato.                                                                       |
| [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Recupera un handle per un contesto di dispositivo di visualizzazione per l'area client di una finestra specificata o per l'intero schermo.                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Recupera l'origine della traduzione finale per un contesto di dispositivo specificato.                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Recupera il colore corrente della penna per il contesto di dispositivo specificato.                                                                         |
| [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Recupera informazioni specifiche del dispositivo per il dispositivo specificato.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Recupera il layout di un contesto di dispositivo.                                                                                                 |
| [**Getobject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Recupera informazioni per l'oggetto grafico specificato.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Recupera il tipo dell'oggetto specificato.                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Recupera un handle per una delle penne, dei pennelli, dei tipi di carattere o delle tavolozze predefinite.                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Rilascia un contesto di dispositivo, liberando il contesto per l'uso da parte di altre applicazioni.                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Aggiorna il contesto di dispositivo della stampante o del tracciatore specificato utilizzando le informazioni specificate.                                                  |
| [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Ripristina lo stato specificato di un contesto di dispositivo.                                                                                         |
| [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Salva lo stato corrente del contesto di dispositivo specificato copiando i dati che descrivono gli oggetti selezionati e le modalità grafiche in uno stack di contesto. |
| [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Seleziona un oggetto nel contesto di dispositivo specificato.                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Imposta il colore del pennello del contesto di dispositivo corrente sul valore di colore specificato.                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Imposta il colore corrente della penna del contesto di dispositivo sul valore di colore specificato.                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Imposta il layout per un contesto di dispositivo.                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Restituisce un handle alla finestra associata a un contesto di dispositivo.                                                                          |



 

 

 
