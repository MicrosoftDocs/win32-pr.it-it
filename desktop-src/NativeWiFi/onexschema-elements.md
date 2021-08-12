---
description: Un profilo 802.1X contiene gli elementi dello schema seguenti.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Elementi dello schema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c20e6bf2b15fa53e5567d02bf3a88135b66fe7de80a171310249ddb941aedb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619986"
---
# <a name="onex-schema-elements"></a>Elementi dello schema OneX

Un profilo 802.1X contiene gli elementi dello schema seguenti. Tutti gli elementi dello schema OneX si applicano ai profili cablati e wireless. La maggior parte degli elementi denominati si trova nello spazio dei nomi , ad eccezione di `https://www.microsoft.com/networking/OneX/v1` [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) che si trova nello spazio dei nomi `https://www.microsoft.com/provisioning/EapHostConfig` .

L'elenco seguente mostra gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo. Viene applicato l'ordinamento degli elementi. Non tutti gli elementi sono in ogni profilo, poiché alcuni elementi sono facoltativi.

Questo elenco non mostra tutti i possibili elementi che possono essere visualizzati in un profilo, perché gli elementi possono essere aggiunti in **xs:any punti** di inserimento.

-   [**Onex**](onexschema-onex-element.md)
    -   [**cacheUserData (OneX)**](onexschema-cacheuserdata-onex-element.md)
    -   [**heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
    -   [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
    -   [**startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
    -   [**maxStart (OneX)**](onexschema-maxstart-onex-element.md)
    -   [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
    -   [**supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
    -   [**authMode (OneX)**](onexschema-authmode-onex-element.md)
    -   [**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
        -   [**type (singleSignOn)**](onexschema-type-singlesignon-element.md)
        -   [**maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md)
        -   [**userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)

 

 



