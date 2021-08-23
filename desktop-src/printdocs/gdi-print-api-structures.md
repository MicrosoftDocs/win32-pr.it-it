---
description: Strutture dell'API di stampa GDI
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: Strutture dell'API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5af0087ed47123b29d6712df2c842a7f05c0d77997df7c3049cc42e0677a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971470"
---
# <a name="gdi-print-api-structures"></a>Strutture dell'API di stampa GDI

## <a name="in-this-section"></a>Contenuto della sezione



| Struttura                                                      | Descrizione                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | La [**struttura dei dati DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) contiene informazioni sull'inizializzazione e sull'ambiente di una stampante o di un dispositivo di visualizzazione. <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | La [**struttura DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) contiene i nomi dei file di input e di output e altre informazioni usate dalla [**funzione StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | La [**struttura DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) definisce un rettangolo da creare.<br/>                                                                                                                                                                         |
| [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | La [**struttura PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) contiene informazioni su un formato carta personalizzato per PostScript driver. Questa struttura viene usata con la [**funzione di escape della stampante GET PS \_ \_ FEATURESETTING.**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85))<br/> |
| [**PSFEATURE \_ OUTPUT**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | La [**struttura PSFEATURE \_ OUTPUT**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) contiene informazioni sulle opzioni di output PostScript driver. Questa struttura viene usata con la [**funzione di escape della stampante GET PS \_ \_ FEATURESETTING.**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85))<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | La [**struttura PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) è un'intestazione per il buffer di input usato con la funzione di escape della stampante [**POSTSCRIPT \_ INJECTION.**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85))<br/>                                                                            |



 

 

