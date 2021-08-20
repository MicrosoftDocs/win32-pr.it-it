---
title: Funzioni server (Windows funzionalità di accessibilità)
description: Funzioni server
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2eb449e81371a1c0c9e230610de97b8abdefb41429c5753059540e45f921d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828069"
---
# <a name="server-functions-windows-accessibility-features"></a>Funzioni server (Windows funzionalità di accessibilità)

Questa sezione contiene informazioni sulle funzioni server usate con Microsoft Active Accessibility.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | Consente a un'applicazione assistive technology (AT) di notificare al sistema che sta interagendo con l'interfaccia utente tramite un'API di automazione di Windows (ad esempio Microsoft Automazione interfaccia utente) come risultato di un movimento tocco da parte dell'utente. Ciò consente al assistive technology di notificare all'applicazione di destinazione e al sistema che l'utente sta interagendo con il tocco.<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Imposta i valori di sistema che indicano se lo stato corrente di un'applicazione assistive technology (AT) influisce sulle funzionalità generalmente fornite dal sistema. <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Crea un oggetto accessibile con i metodi e le proprietà del tipo specificato di elemento dell'interfaccia utente fornito dal sistema.<br/>                                                                                                                                                                                                                      |
| [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Crea un oggetto accessibile che dispone delle proprietà e dei metodi della classe specificata dell'elemento dell'interfaccia utente fornito dal sistema.<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Restituisce un riferimento, simile a un handle, all'oggetto specificato. I server restituiscono questo riferimento durante la [**gestione di WM \_ GETOBJECT**](wm-getobject.md).<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Recupera un puntatore a interfaccia richiesto per un oggetto accessibile in base a un riferimento a un oggetto generato in precedenza.<br/> Questa funzione è progettata per l'uso interno da Microsoft Active Accessibility ed è documentata solo a scopo informativo. Né i client né i server devono chiamare questa funzione.<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Determina se è presente un hook WinEvent installato che potrebbe ricevere una notifica di un evento specificato.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Segnala al sistema che si è verificato un evento predefinito. Se le applicazioni client hanno registrato una funzione hook per l'evento, il sistema chiama la funzione hook del client.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Active Accessibility Interfaccia utente Services](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





