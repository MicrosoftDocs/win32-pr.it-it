---
description: Le informazioni utente sono un buffer che può essere trasmesso da un'estremità di una connessione a un'altra. Queste informazioni sono specifiche dello standard ISDN Q.931. Fare riferimento alla documentazione dei provider di servizi sul significato e sull'uso di questi dati.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Informazioni utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203b0b466d1b0b3f9da93cfefc5da737865da3cf5d40921dae6c969bfc9b9752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975291"
---
# <a name="user-user-information"></a>Informazioni utente

Le informazioni utente sono un buffer che può essere trasmesso da un'estremità di una connessione a un'altra. Queste informazioni sono specifiche dello standard ISDN Q.931. Fare riferimento alla documentazione del provider di servizi sul significato e sull'uso di questi dati.

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x: **[**lineGetCallInfo,**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) **dwCallDataSize** e **dwCallDataOffset** membri di [**LINECALLINFO,**](/windows/win32/api/tapi/ns-tapi-linecallinfo) [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

**TAPI 3.x: **[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), chiamato con il membro **CIB \_ USERUSERINFO** di [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
