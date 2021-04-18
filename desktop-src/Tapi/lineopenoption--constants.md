---
description: Le \_ costanti LINEOPENOPTION elencano le opzioni disponibili per l'apertura di una riga.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Costanti LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331256"
---
# <a name="lineopenoption_-constants"></a><span data-ttu-id="aca0f-103">\_Costanti LINEOPENOPTION</span><span class="sxs-lookup"><span data-stu-id="aca0f-103">LINEOPENOPTION\_ Constants</span></span>

<span data-ttu-id="aca0f-104">Le **\_ costanti LINEOPENOPTION** elencano le opzioni disponibili per l'apertura di una riga.</span><span class="sxs-lookup"><span data-stu-id="aca0f-104">The **LINEOPENOPTION\_ constants** list the available options for opening a line.</span></span>

<dl> <dt>

<span data-ttu-id="aca0f-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**</span><span class="sxs-lookup"><span data-stu-id="aca0f-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="aca0f-106">L'applicazione è pronta a gestire le richieste provenienti da altre applicazioni con la riga aperta.</span><span class="sxs-lookup"><span data-stu-id="aca0f-106">The application is willing to handle requests from other applications that have the line open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aca0f-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**\_SINGLEADDRESS LINEOPENOPTION**</span><span class="sxs-lookup"><span data-stu-id="aca0f-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION\_SINGLEADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="aca0f-108">L'applicazione deve essere informata sulle nuove chiamate create sul dispositivo di linea solo se tali chiamate vengono visualizzate nell'indirizzo specificato nel membro **dwAddressID** della struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) a cui punta il parametro *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="aca0f-108">The application should be informed of new calls created on the line device only if those calls appear on the address specified in the **dwAddressID** member in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aca0f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="aca0f-109">Remarks</span></span>

<span data-ttu-id="aca0f-110">Per ulteriori informazioni sul funzionamento di queste opzioni, vedere [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .</span><span class="sxs-lookup"><span data-stu-id="aca0f-110">See [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca0f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aca0f-111">Requirements</span></span>



| <span data-ttu-id="aca0f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aca0f-112">Requirement</span></span> | <span data-ttu-id="aca0f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aca0f-113">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="aca0f-114">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="aca0f-114">TAPI version</span></span><br/> | <span data-ttu-id="aca0f-115">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="aca0f-115">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="aca0f-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aca0f-116">Header</span></span><br/>       | <dl> <span data-ttu-id="aca0f-117"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca0f-117"><dt>Tapi.h</dt></span></span> </dl> |



 

 




