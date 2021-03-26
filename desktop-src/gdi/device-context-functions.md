---
description: Le funzioni seguenti vengono usate con i contesti di dispositivo.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Funzioni di contesto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625b81b999526d84af4b58f2dddbc280643bcd35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754458"
---
# <a name="device-context-functions"></a>Funzioni di contesto del dispositivo

Le funzioni seguenti vengono usate con i contesti di dispositivo.



| Funzione                                                   | Descrizione                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Annulla tutte le operazioni in sospeso nel contesto di dispositivo specificato.                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Modifica le impostazioni del dispositivo di visualizzazione predefinito nella modalità grafica specificata.                                                        |
| [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Modifica le impostazioni del dispositivo di visualizzazione specificato nella modalità grafica specificata.                                                      |
| [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Crea un contesto di dispositivo di memoria compatibile con il dispositivo specificato.                                                                     |
| [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Crea un contesto di dispositivo per un dispositivo usando il nome specificato.                                                                           |
| [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Crea un contesto delle informazioni per il dispositivo specificato.                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Elimina il contesto di dispositivo specificato.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Elimina una penna logica, un pennello, un tipo di carattere, una bitmap, un'area o una tavolozza, liberando tutte le risorse di sistema associate all'oggetto.                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Recupera le funzionalità di un driver di dispositivo stampante.                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Fornisce funzionalità di disegno dello schermo video specificato che non sono direttamente disponibili tramite l'interfaccia grafica del dispositivo.       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Recupera le informazioni sui dispositivi di visualizzazione in un sistema.                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Recupera le informazioni su una delle modalità grafiche per un dispositivo di visualizzazione.                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Recupera le informazioni su una delle modalità grafiche per un dispositivo di visualizzazione.                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Enumera le penne o i pennelli disponibili per il contesto di dispositivo specificato.                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Funzione di callback definita dall'applicazione utilizzata con la funzione [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .                                       |
| [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Recupera un handle per un oggetto del tipo specificato selezionato nel contesto di dispositivo specificato.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Recupera un handle per un contesto di periferica di visualizzazione per l'area client di una finestra specificata o per l'intera schermata.                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Recupera il colore corrente del pennello per il contesto di dispositivo specificato.                                                                       |
| [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Recupera un handle per un contesto di periferica di visualizzazione per l'area client di una finestra specificata o per l'intera schermata.                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Recupera l'origine di conversione finale per un contesto di dispositivo specificato.                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Recupera il colore corrente della penna per il contesto di dispositivo specificato.                                                                         |
| [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Recupera le informazioni specifiche del dispositivo per il dispositivo specificato.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Recupera il layout di un contesto di dispositivo.                                                                                                 |
| [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Recupera le informazioni per l'oggetto Graphics specificato.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Recupera il tipo dell'oggetto specificato.                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Recupera un handle per una delle penne predefinite, i pennelli, i tipi di carattere o le tavolozze.                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Rilascia un contesto di dispositivo, liberando l'uso da altre applicazioni.                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Aggiorna il contesto di dispositivo della stampante o del plotter specificato utilizzando le informazioni specificate.                                                  |
| [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Ripristina un contesto di dispositivo nello stato specificato.                                                                                         |
| [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Salva lo stato corrente del contesto di dispositivo specificato copiando i dati che descrivono gli oggetti selezionati e le modalità grafiche in uno stack di contesti. |
| [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Seleziona un oggetto nel contesto di dispositivo specificato.                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Imposta il colore del pennello del contesto di dispositivo corrente sul valore del colore specificato.                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Imposta il colore corrente della penna del contesto del dispositivo sul valore del colore specificato.                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Imposta il layout per un contesto di dispositivo.                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Restituisce un handle per la finestra associata a un contesto di dispositivo.                                                                          |



 

 

 
