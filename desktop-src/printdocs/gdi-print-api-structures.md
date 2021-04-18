---
description: Strutture API di stampa GDI
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: Strutture API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ae427af0112061e6b90afa71cc2b65427d477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314994"
---
# <a name="gdi-print-api-structures"></a>Strutture API di stampa GDI

## <a name="in-this-section"></a>Contenuto della sezione



| Struttura                                                      | Descrizione                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | La struttura dei dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) contiene informazioni sull'inizializzazione e l'ambiente di una stampante o di un dispositivo di visualizzazione. <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | La struttura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) contiene i nomi dei file di input e di output e altre informazioni utilizzate dalla funzione [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | La struttura [**DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) definisce un rettangolo da creare.<br/>                                                                                                                                                                         |
| [**\_CUSTPAPER PSFEATURE**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | La struttura [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) contiene informazioni su un formato cartaceo personalizzato per un driver PostScript. Questa struttura viene utilizzata con la funzione [**get \_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) Printer escape.<br/> |
| [**\_output PSFEATURE**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | La struttura di [**\_ output PSFEATURE**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) contiene informazioni sulle opzioni di output del driver PostScript. Questa struttura viene utilizzata con la funzione [**get \_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) Printer escape.<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | La struttura [**PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) è un'intestazione per il buffer di input usato con la funzione di escape della stampante di [**\_ inserimento**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)) di post-script.<br/>                                                                            |



 

 

