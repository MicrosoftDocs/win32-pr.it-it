---
title: Procedure consigliate per l'uso Cassaforte matrici
description: Molti metodi di interfaccia di Microsoft Automazione interfaccia utente \ 32; Argomenti di api take denominati matrici sicure, del tipo di dati SAFEARRAY. In questo argomento vengono descritte le procedure consigliate per l'uso di matrici sicure in Automazione interfaccia utente applicazioni.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automazione interfaccia utente, matrici sicure
- Automazione interfaccia utente,providers
- Automazione interfaccia utente,client
- Automazione interfaccia utente,conversione tra tipi di dati
- client, matrici sicure
- providers,Automazione interfaccia utente
- matrici sicure
- tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ea76358f3a547b4364d01f56e850d0cbb523fc35dfbaa2870448f70c6ad5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098121"
---
# <a name="best-practices-for-using-safe-arrays"></a>Procedure consigliate per l'uso Cassaforte matrici

Molti metodi di interfaccia dell'API microsoft Automazione interfaccia utente accettano argomenti denominati matrici sicure, del tipo di dati [**SAFEARRAY.**](/windows/win32/api/oaidl/ns-oaidl-safearray) In questo argomento vengono descritte le procedure consigliate per l'uso di matrici sicure in Automazione interfaccia utente applicazioni.

## <a name="clients"></a>Client

Tutte le matrici sicure usate con i Automazione interfaccia utente api client sono matrici unidimensionali in base zero. Per creare una matrice sicura per un metodo client Automazione interfaccia utente, usare la funzione [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) e per leggere e scrivere in una matrice sicura, usare le funzioni [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) e [**SafeArrayPutElement.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) Al termine dell'uso di una matrice sicura, eliminarla sempre usando la funzione [**SafeArrayDestroy,**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) sia che sia stata creata o ricevuta da un metodo client Automazione interfaccia utente safe.

Diversi Automazione interfaccia utente, inclusi i metodi di recupero delle proprietà, ad esempio [**GetCurrentPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)recuperano [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)che possono contenere strutture [**POINT**](/previous-versions//dd162805(v=vs.85)) o [**UiaRect.**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) Un **punto** viene inserito in un **elemento VARIANT** come matrice sicura di valori double (VT R8) con il membro x in corrispondenza dell'indice 0 e il membro y in corrispondenza dell'indice \_ 1.   Analogamente, **un oggetto UiaRect** viene inserito in un elemento **VARIANT** come matrice sicura di valori double con i membri **left,** **top,** **width** e **height** in corrispondenza rispettivamente degli indici da 0 a 3. Per una matrice **di strutture UiaRect,** la matrice sicura contiene una matrice sequenziale di quattro valori double per **ogni UiaRect**. I **membri left**, **top**, **width** e **height** del primo **oggetto UiaRect** occupano l'indice da 0 a 3, i membri del secondo rettangolo occupano l'indice da 4 a 7 e così via.

[**L'interfaccia IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) include i metodi seguenti per la conversione tra [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) e vari altri tipi di dati.



| Metodo                                                                                               | Descrizione                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Converte una matrice di numeri interi in [**safearray**](/windows/win32/api/oaidl/ns-oaidl-safearray).                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Converte un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di numeri interi in una matrice.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Converte un [**oggetto SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) che contiene coordinate rettangolari in una matrice di tipo **RECT.** |



 

## <a name="providers"></a>Provider

Un provider deve implementare una serie di metodi di interfaccia che Automazione interfaccia utente chiamate per recuperare informazioni dal provider. Molte volte, queste informazioni sono costituite da una matrice di valori. Per restituire una matrice Automazione interfaccia utente, il provider deve creare un pacchetto della matrice in una [**struttura SAFEARRAY.**](/windows/win32/api/oaidl/ns-oaidl-safearray) Gli elementi della matrice devono essere del tipo di dati previsto e devono essere visualizzati nell'ordine previsto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Nozioni fondamentali sull'automazione interfaccia utente](entry-uiautocore-overview.md)
</dt> </dl>

 

 