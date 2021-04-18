---
title: Procedure consigliate per l'utilizzo di matrici sicure
description: Molti metodi di interfaccia di automazione interfaccia utente Microsoft \ 32; API accettano gli argomenti chiamati matrici sicure del tipo di dati SAFEARRAY. In questo argomento vengono descritte le procedure consigliate per l'utilizzo di matrici sicure in un'applicazione di automazione interfaccia utente.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automazione interfaccia utente, matrici sicure
- Automazione interfaccia utente, provider
- Automazione interfaccia utente, client
- Automazione interfaccia utente, conversione tra tipi di dati
- client, matrici sicure
- provider, automazione interfaccia utente
- matrici sicure
- tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300169"
---
# <a name="best-practices-for-using-safe-arrays"></a>Procedure consigliate per l'utilizzo di matrici sicure

Molti metodi di interfaccia dell'API di automazione interfaccia utente Microsoft accettano gli argomenti chiamati matrici sicure del tipo di dati [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) . In questo argomento vengono descritte le procedure consigliate per l'utilizzo di matrici sicure in un'applicazione di automazione interfaccia utente.

## <a name="clients"></a>Client

Tutte le matrici sicure usate con i metodi dell'API client di automazione interfaccia utente sono matrici unidimensionali in base zero. Per creare una matrice sicura per un metodo client di automazione interfaccia utente, usare la funzione [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) e per leggere e scrivere in una matrice sicura, usare le funzioni [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) e [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) . Al termine dell'uso di un array sicuro, eliminarlo sempre usando la funzione [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , se è stata creata la matrice sicura o ricevuta da un metodo client di automazione interfaccia utente.

Diversi metodi di automazione interfaccia utente, inclusi i metodi di recupero delle proprietà, ad esempio [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), recuperano le [**varianti**](/windows/win32/api/oaidl/ns-oaidl-variant)che possono contenere strutture [**Point**](/previous-versions//dd162805(v=vs.85)) o [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) . Un **punto** viene compresso in una **variante** come una matrice sicura di doppi (VT \_ R8) con il membro **x** in corrispondenza dell'indice 0 e il membro **y** in corrispondenza dell'indice 1. Analogamente, un **UiaRect** viene compresso in una **variante** come matrice sicura di Double con i membri **Left**, **Top**, **Width** e **Height** rispettivamente negli indici da 0 a 3. Per una matrice di strutture **UiaRect** , la matrice sicura contiene una matrice sequenziale di quattro doppi per ogni **UiaRect**. I membri **Left**, **Top**, **Width** e **Height** del primo **UiaRect** occupano l'indice da 0 a 3, i membri del secondo rettangolo occupano l'indice da 4 a 7 e così via.

L'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) include i metodi seguenti per la conversione tra [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) e diversi altri tipi di dati.



| Metodo                                                                                               | Descrizione                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Converte una matrice di numeri interi in un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Converte un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di interi in una matrice.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Converte un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) che contiene Coordinate rettangolo in una matrice di tipo **Rect**. |



 

## <a name="providers"></a>Provider

Un provider deve implementare una serie di metodi di interfaccia chiamati da automazione interfaccia utente per recuperare le informazioni dal provider. Molte volte tali informazioni sono costituite da una matrice di valori. Per restituire una matrice all'automazione interfaccia utente, il provider deve comprimere la matrice in una struttura [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) . Gli elementi della matrice devono essere del tipo di dati previsto e devono essere visualizzati nell'ordine previsto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Nozioni fondamentali sull'automazione interfaccia utente](entry-uiautocore-overview.md)
</dt> </dl>

 

 