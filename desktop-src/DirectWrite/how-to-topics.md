---
title: Procedure (DirectWrite)
description: Negli argomenti seguenti viene fornita una panoramica dell'API DirectWrite.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26bbb4500ab016fbf5a5a59f6b551030e28dd1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047740"
---
# <a name="how-to-topics-directwrite"></a>Procedure (DirectWrite)

Negli argomenti seguenti viene fornita una panoramica dell'API [DirectWrite](direct-write-portal.md) .

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come allineare il testo](how-to-align-text.md)<br/>                                                                                                                   | È possibile allineare il testo [DirectWrite](direct-write-portal.md) usando il metodo [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) dell'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)<br/>                                                                                                                                                                                                               |
| [Come aggiungere il supporto per più monitoraggi](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) include il supporto per i sistemi con più monitor. Diversi monitoraggi possono avere una geometria di pixel diversa (RGB, BGR o FLAT) o altri attributi. Per ulteriori informazioni sulla geometria dei pixel, vedere l'argomento di riferimento sulla [**\_ \_ geometria dei pixel DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . In questo argomento viene illustrato come aggiungere il supporto per più monitoraggi all'applicazione DirectWrite. <br/> |
| [Come verificare che l'applicazione venga visualizzata correttamente su schermi con DPI elevato](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Viene descritto come creare una finestra visualizzata correttamente su schermi a DPI elevato.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Come verificare che il testo venga visualizzato con la direzione di lettura corretta](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Alcuni linguaggi, come l'arabo e l'ebraico, richiedono una direzione di lettura da destra a sinistra. Per un oggetto in formato testo [DirectWrite](direct-write-portal.md) , la direzione di lettura predefinita è da sinistra a destra. DirectWrite non deduce automaticamente la direzione di lettura dalle impostazioni locali, quindi è necessario eseguire questa operazione manualmente.<br/>                                                                                                   |
| [Come enumerare i tipi di carattere](font-enumeration.md)<br/>                                                                                                               | In questa panoramica viene illustrato come enumerare i tipi di carattere nella raccolta di tipi di carattere del sistema, in base al nome della famiglia.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Come eseguire l'hit testing in un layout di testo](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Viene fornita una breve esercitazione su come aggiungere l'hit test a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo tramite l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                  |
| [Come aggiungere oggetti inline a un layout di testo](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Fornisce una breve esercitazione sull'aggiunta di oggetti inline a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                         |
| [Come aggiungere effetti di disegno client a un layout di testo](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Fornisce una breve esercitazione sull'aggiunta di effetti di disegno dei client a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e un renderer di testo personalizzato. <br/>                                                                                                                                                                                      |



 

 

