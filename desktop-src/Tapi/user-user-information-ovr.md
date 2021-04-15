---
description: Informazioni utente utente è un buffer che può essere trasmesso da un'estremità di una connessione a un'altra. Queste informazioni sono specifiche dello standard ISDN Q. 931. Per informazioni sul significato e sull'uso di questi dati, fare riferimento alla documentazione del provider di servizi.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Informazioni utente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529706"
---
# <a name="user-user-information"></a>Informazioni utente utente

Informazioni utente utente è un buffer che può essere trasmesso da un'estremità di una connessione a un'altra. Queste informazioni sono specifiche dello standard ISDN Q. 931. Per informazioni sul significato e sull'uso di questi dati, vedere la documentazione del provider di servizi.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** e **dwCallDataOffset** membri di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

* * TAPI 3. x: * *[**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), chiamato con il **membro \_ USERUSERINFO di CIB** di [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo:: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
