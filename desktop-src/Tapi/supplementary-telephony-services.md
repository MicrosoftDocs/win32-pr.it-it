---
description: I servizi di telefonia supplementare sono la raccolta di tutti i servizi definiti dall'API, ad eccezione di quelli inclusi nel sottoinsieme telefonico di base.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Servizi di telefonia supplementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d93a7d12840e2001c6a2742e6bbd870d291e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881634"
---
# <a name="supplementary-telephony-services"></a>Servizi di telefonia supplementari

I servizi di telefonia supplementare sono la raccolta di tutti i servizi definiti dall'API, ad eccezione di quelli inclusi nel sottoinsieme telefonico di base. Sono incluse tutte le cosiddette funzionalità supplementari disponibili sui PBX moderni, ad esempio l'attesa, il trasferimento, la conferenza, il parco e così via. Tutte le funzionalità supplementari sono considerate facoltative; ovvero, il provider di servizi decide quale di questi servizi ha o non fornisce.

Un'applicazione può eseguire una query su una linea o un dispositivo telefonico per il set di servizi supplementari che fornisce usando funzioni quali [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) o [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps). Un singolo servizio supplementare può essere costituito da più chiamate di funzione e messaggi. L'API di telefonia, e non lo sviluppatore del provider di servizi, definisce il comportamento di ognuna di queste funzionalità supplementari. Un provider di servizi deve fornire un servizio di telefonia supplementare solo se può implementare il significato esatto definito dall'API. In caso contrario, la funzionalità deve essere fornita come servizio di telefonia estesa.

Come indicato nei servizi telefonici di base, i servizi del dispositivo telefonico sono considerati facoltativi. Pertanto, tutti i servizi per dispositivi telefonici fanno parte della telefonia supplementare. Per un elenco delle funzioni di telefonia supplementare, vedere informazioni di [riferimento sulle funzioni TAPI Quick](./tapi-quick-function-reference.md).

 

 
