---
description: Il tipo di indirizzo identifica il formato necessario per un indirizzo. Ad esempio, se il tipo è LINEADDRESSTYPE \_ PhoneNumber, l'indirizzo usato per comporre la sessione deve essere un numero di telefono.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Tipo di indirizzo per una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312734"
---
# <a name="address-type-for-a-session"></a>Tipo di indirizzo per una sessione

Il [**tipo di indirizzo**](lineaddresstype--constants.md) identifica il formato necessario per un indirizzo. Ad esempio, se il tipo è LINEADDRESSTYPE \_ PhoneNumber, l'indirizzo usato per comporre la sessione deve essere un numero di telefono.

Un determinato provider di servizi e dispositivi supporta uno o più tipi di indirizzi. Per informazioni su come eseguire il polling di un dispositivo per i formati di indirizzi supportati, vedere [tipi di indirizzi per un dispositivo](address-type-ovr.md) .

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), membro **dwAddressType** di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chiamato con il **membro \_ CIL CALLERIDADDRESSTYPE**, **CIL \_ CALLEDIDADDRESSTYPE** o **CIL \_ CONNECTEDIDADDRESSTYPE** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
