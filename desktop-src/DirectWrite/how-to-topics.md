---
title: Procedure (DirectWrite)
description: Vedere gli argomenti relativi alle procedure nella guida per la programmazione DirectWrite API. DirectWrite consente alle Windows di migliorare l'esperienza di testo per l'interfaccia utente e i documenti.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42848fbf00e099926763f0db54338f3a87ff583782b939f8250a1aabb2b73ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048861"
---
# <a name="how-to-topics-directwrite"></a>Procedure (DirectWrite)

Negli argomenti seguenti viene fornita una panoramica dell'API [DirectWrite.](direct-write-portal.md)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come allineare il testo](how-to-align-text.md)<br/>                                                                                                                   | È possibile [allineare DirectWrite](direct-write-portal.md) testo usando il [**metodo SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) dell'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)<br/>                                                                                                                                                                                                               |
| [Come aggiungere il supporto per più monitoraggi](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) include il supporto per i sistemi con più monitor. Monitor diversi possono avere geometrie pixel diverse (RGB, BGR o FLAT) o altri attributi. Per altre informazioni sulla geometria dei pixel, vedere l'argomento [**di riferimento DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) Questo argomento illustra come aggiungere il supporto per più monitoraggi all DirectWrite applizione. <br/> |
| [Come assicurarsi che l'applicazione venga visualizzata correttamente su schermi con valori DPI elevati](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Viene descritto come creare una finestra visualizzata correttamente su schermi con valori DPI elevati.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Come assicurarsi che il testo sia visualizzato con la direzione di lettura corretta](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Alcune lingue, ad esempio arabo ed ebraico, richiedono una direzione di lettura da destra a sinistra. Per un oggetto [DirectWrite](direct-write-portal.md) formato testo, la direzione di lettura predefinita è da sinistra a destra. DirectWrite non deduce automaticamente la direzione di lettura dalle impostazioni locali, pertanto è necessario eseguire questa operazione manualmente.<br/>                                                                                                   |
| [Come enumerare i tipi di carattere](font-enumeration.md)<br/>                                                                                                               | Questa panoramica illustra come enumerare i tipi di carattere nella raccolta di tipi di carattere di sistema, in base al nome della famiglia.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Come eseguire l'hit testing in un layout di testo](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Viene fornita una breve esercitazione su come aggiungere hit testing a [un'applicazione DirectWrite](direct-write-portal.md) che visualizza testo usando l'interfaccia [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) <br/>                                                                                                                                                                                                                  |
| [Come aggiungere oggetti inline a un layout di testo](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Viene fornita una breve esercitazione sull'aggiunta di oggetti inline a [un'DirectWrite](direct-write-portal.md) che visualizza testo usando [**l'interfaccia IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) <br/>                                                                                                                                                                                                                         |
| [Come aggiungere effetti di disegno client a un layout di testo](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Viene fornita una breve esercitazione sull'aggiunta di effetti di disegno client a un'applicazione [DirectWrite](direct-write-portal.md) che visualizza testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e un renderer di testo personalizzato. <br/>                                                                                                                                                                                      |



 

 

