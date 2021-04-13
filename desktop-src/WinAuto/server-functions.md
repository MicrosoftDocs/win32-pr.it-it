---
title: Funzioni server (funzionalità di accessibilità di Windows)
description: Funzioni server
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a747c073e84049fe578d19561b25d0b754dbb9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400184"
---
# <a name="server-functions-windows-accessibility-features"></a>Funzioni server (funzionalità di accessibilità di Windows)

In questa sezione vengono fornite informazioni sulle funzioni server utilizzate con Microsoft Active Accessibility.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | Consente a un'applicazione Assistive Technology (AT) di notificare al sistema che interagisce con l'interfaccia utente tramite un'API di automazione di Windows, ad esempio l'automazione interfaccia utente Microsoft, a seguito di un gesto tocco dall'utente. In questo modo, la tecnologia per l'accessibilità invia una notifica all'applicazione di destinazione e al sistema con cui l'utente interagisce con il tocco.<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Imposta i valori di sistema che indicano se lo stato corrente di un'applicazione Assistive Technology (AT) influiscono sulla funzionalità fornita in genere dal sistema. <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Crea un oggetto accessibile con i metodi e le proprietà del tipo specificato di elemento dell'interfaccia utente fornito dal sistema.<br/>                                                                                                                                                                                                                      |
| [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Crea un oggetto accessibile che dispone delle proprietà e dei metodi della classe specificata dell'elemento dell'interfaccia utente fornito dal sistema.<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Restituisce un riferimento, simile a un handle, all'oggetto specificato. I server restituiscono questo riferimento quando si gestisce [**WM \_ GetObject**](wm-getobject.md).<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Recupera un puntatore a interfaccia richiesto per un oggetto accessibile in base a un riferimento a un oggetto generato in precedenza.<br/> Questa funzione è progettata per l'uso interno da Microsoft Active Accessibility ed è documentata solo a scopo informativo. Né i client né i server devono chiamare questa funzione.<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Determina se è presente un hook WinEvent installato che può ricevere una notifica di un evento specificato.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Segnala al sistema che si è verificato un evento predefinito. Se un'applicazione client ha registrato una funzione hook per l'evento, il sistema chiama la funzione hook del client.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi interfaccia utente Active Accessibility](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





