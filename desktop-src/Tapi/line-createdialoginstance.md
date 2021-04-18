---
description: Il messaggio TSPI LINE \_ CREATEDIALOGINSTANCE fa in modo che TAPI crei un'associazione tra il provider di servizi e un'istanza della \_ funzione TUISPI providerGenericDialog in esecuzione nel contesto dell'applicazione.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Messaggio LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328050"
---
# <a name="line_createdialoginstance-message"></a><span data-ttu-id="8e209-103">\_Messaggio linea CREATEDIALOGINSTANCE</span><span class="sxs-lookup"><span data-stu-id="8e209-103">LINE\_CREATEDIALOGINSTANCE message</span></span>

<span data-ttu-id="8e209-104">Il messaggio **TSPI \_ line CREATEDIALOGINSTANCE** fa in modo che TAPI crei un'associazione tra il provider di servizi e un'istanza della funzione [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) in esecuzione nel contesto dell'applicazione che ha richiamato la funzione asincrona TSPI identificata dal parametro *DwRequestID* della struttura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) a cui punta *lpTUISPICreateDialogInstanceParams*.</span><span class="sxs-lookup"><span data-stu-id="8e209-104">The TSPI **LINE\_CREATEDIALOGINSTANCE** message causes TAPI to create an association between the service provider and an instance of the [**TUISPI\_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) function executing in the context of the application that invoked the asynchronous TSPI function identified by the *dwRequestID* parameter of the [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure pointed to by *lpTUISPICreateDialogInstanceParams*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8e209-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e209-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e209-106">*hProvider*</span><span class="sxs-lookup"><span data-stu-id="8e209-106">*hProvider*</span></span> 
</dt> <dd>

<span data-ttu-id="8e209-107">ProviderHandle fornito al provider di servizi come parametro per [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span><span class="sxs-lookup"><span data-stu-id="8e209-107">The ProviderHandle supplied to the service provider as a parameter to [**TSPI\_providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span></span>

</dd> <dt>

<span data-ttu-id="8e209-108">*lpTUISPICreateDialogInstanceParams*</span><span class="sxs-lookup"><span data-stu-id="8e209-108">*lpTUISPICreateDialogInstanceParams*</span></span> 
</dt> <dd>

<span data-ttu-id="8e209-109">Puntatore a una struttura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .</span><span class="sxs-lookup"><span data-stu-id="8e209-109">Pointer to a [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e209-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e209-110">Requirements</span></span>



| <span data-ttu-id="8e209-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e209-111">Requirement</span></span> | <span data-ttu-id="8e209-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8e209-112">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8e209-113">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="8e209-113">TAPI version</span></span><br/> | <span data-ttu-id="8e209-114">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8e209-114">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8e209-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e209-115">Header</span></span><br/>       | <dl> <span data-ttu-id="8e209-116"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e209-116"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e209-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e209-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e209-118">**\_PROVIDERENUMDEVICES TSPI**</span><span class="sxs-lookup"><span data-stu-id="8e209-118">**TSPI\_providerEnumDevices**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[<span data-ttu-id="8e209-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="8e209-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

