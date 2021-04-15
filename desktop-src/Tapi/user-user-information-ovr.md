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
# <a name="user-user-information"></a><span data-ttu-id="09c03-105">Informazioni utente utente</span><span class="sxs-lookup"><span data-stu-id="09c03-105">User-user information</span></span>

<span data-ttu-id="09c03-106">Informazioni utente utente è un buffer che può essere trasmesso da un'estremità di una connessione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="09c03-106">User-user information is a buffer that can be transmitted from one end of a connection to another.</span></span> <span data-ttu-id="09c03-107">Queste informazioni sono specifiche dello standard ISDN Q. 931.</span><span class="sxs-lookup"><span data-stu-id="09c03-107">This information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="09c03-108">Per informazioni sul significato e sull'uso di questi dati, vedere la documentazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="09c03-108">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="09c03-109">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="09c03-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="09c03-110">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** e **dwCallDataOffset** membri di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="09c03-110">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span></span>

<span data-ttu-id="09c03-111">\* \* TAPI 3. x: \* \*[**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), chiamato con il **membro \_ USERUSERINFO di CIB** di [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo:: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="09c03-111">\*\*TAPI 3.x:  \*\*[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), called with the **CIB\_USERUSERINFO** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span></span>

 

 
