---
description: Il messaggio della riga TSPI \_ SENDDIALOGINSTANCEDATA fa in modo che TAPI chiami la \_ funzione PROVIDERGENERICDIALOGDATA di TUISPI nella DLL dell'interfaccia utente associata a htDlgInst, passando al blocco di parametri a cui punta lpParams, di lunghezza dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Messaggio LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332917"
---
# <a name="line_senddialoginstancedata-message"></a><span data-ttu-id="5db5b-103">\_Messaggio linea SENDDIALOGINSTANCEDATA</span><span class="sxs-lookup"><span data-stu-id="5db5b-103">LINE\_SENDDIALOGINSTANCEDATA message</span></span>

<span data-ttu-id="5db5b-104">Il messaggio della **riga TSPI \_ SENDDIALOGINSTANCEDATA** fa in modo che TAPI chiami la funzione [**\_ providerGenericDialogData di TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) nella DLL dell'interfaccia utente associata a *htDlgInst*, passando al blocco di parametri a cui punta *lpParams*, di lunghezza *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="5db5b-104">The TSPI **LINE\_SENDDIALOGINSTANCEDATA** message causes TAPI to call the [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function in the UI DLL associated with *htDlgInst*, passing it the parameter block pointed to by *lpParams*, of length *dwSize*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5db5b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="5db5b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db5b-106">*htDlgInst*</span><span class="sxs-lookup"><span data-stu-id="5db5b-106">*htDlgInst*</span></span> 
</dt> <dd>

<span data-ttu-id="5db5b-107">HTAPIDIALOGINSTANCE restituito al provider di servizi quando l'istanza della finestra di dialogo è stata creata utilizzando la [**riga \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span><span class="sxs-lookup"><span data-stu-id="5db5b-107">The HTAPIDIALOGINSTANCE that was returned to the service provider when the dialog box instance was created using [**LINE\_CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="5db5b-108">*lpParams*</span><span class="sxs-lookup"><span data-stu-id="5db5b-108">*lpParams*</span></span> 
</dt> <dd>

<span data-ttu-id="5db5b-109">Puntatore a un blocco di parametri specifico del provider trasmesso alla funzione [**TUISPI \_ PROVIDERGENERICDIALOGDATA**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) della DLL dell'interfaccia utente, la cui dimensione è specificata da *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="5db5b-109">Pointer to a provider-specific parameter block that is conveyed to the UI DLL [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function, the size of which is specified by *dwSize*.</span></span> <span data-ttu-id="5db5b-110">Se questo parametro è impostato su **null**, si tratta di una richiesta di chiusura immediata della finestra di dialogo e di pulizia (la DLL dell'interfaccia utente non deve richiamare [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante questa pulitura).</span><span class="sxs-lookup"><span data-stu-id="5db5b-110">If this parameter is set to **NULL**, this is a request to close the dialog box immediately and clean up (the UI DLL should not invoke [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) during this cleanup).</span></span>

</dd> <dt>

<span data-ttu-id="5db5b-111">*dwSize*</span><span class="sxs-lookup"><span data-stu-id="5db5b-111">*dwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="5db5b-112">Dimensioni in byte del blocco di parametri da trasferire alla DLL dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5db5b-112">The size in bytes of the parameter block to be conveyed to the UI DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5db5b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5db5b-113">Requirements</span></span>



| <span data-ttu-id="5db5b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5db5b-114">Requirement</span></span> | <span data-ttu-id="5db5b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5db5b-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5db5b-116">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5db5b-116">TAPI version</span></span><br/> | <span data-ttu-id="5db5b-117">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5db5b-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5db5b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5db5b-118">Header</span></span><br/>       | <dl> <span data-ttu-id="5db5b-119"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5db5b-119"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db5b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5db5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db5b-121">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="5db5b-121">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[<span data-ttu-id="5db5b-122">**\_PROVIDERGENERICDIALOGDATA TUISPI**</span><span class="sxs-lookup"><span data-stu-id="5db5b-122">**TUISPI\_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[<span data-ttu-id="5db5b-123">**LINEA \_ CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="5db5b-123">**LINE\_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
</dt> </dl>

 

