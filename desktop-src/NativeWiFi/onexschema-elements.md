---
description: Un profilo 802.1 X contiene i seguenti elementi dello schema.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Elementi dello schema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756458"
---
# <a name="onex-schema-elements"></a>Elementi dello schema OneX

Un profilo 802.1 X contiene i seguenti elementi dello schema. Tutti gli elementi dello schema OneX si applicano ai profili cablati e wireless. La maggior parte degli elementi denominati si trova nello spazio dei nomi `https://www.microsoft.com/networking/OneX/v1` , ad eccezione di [**EAPConfig (Onex)**](onexschema-eapconfig-onex-element.md) , che si trova nello spazio dei nomi `https://www.microsoft.com/provisioning/EapHostConfig` .

Nell'elenco seguente vengono illustrati gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo. Viene applicato l'ordinamento degli elementi. Non tutti gli elementi sono in tutti i profili, perché alcuni elementi sono facoltativi.

Questo elenco non Mostra tutti i possibili elementi che possono essere visualizzati in un profilo, perché è possibile aggiungere elementi in **xs: qualsiasi** punto di inserimento.

-   [**OneX**](onexschema-onex-element.md)
    -   [**cacheUserData (OneX)**](onexschema-cacheuserdata-onex-element.md)
    -   [**heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
    -   [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
    -   [**startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
    -   [**maxStart (OneX)**](onexschema-maxstart-onex-element.md)
    -   [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
    -   [**supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
    -   [**authMode (OneX)**](onexschema-authmode-onex-element.md)
    -   [**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
        -   [**tipo (singleSignOn)**](onexschema-type-singlesignon-element.md)
        -   [**maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md)
        -   [**userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)

 

 



