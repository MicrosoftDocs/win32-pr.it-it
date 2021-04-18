---
description: Le \_ costanti del flag di bit LINEADDRESSMODE descrivono diversi modi per identificare un indirizzo in un dispositivo a linee.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Costanti LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328420"
---
# <a name="lineaddressmode_-constants"></a><span data-ttu-id="7353c-103">\_Costanti LINEADDRESSMODE</span><span class="sxs-lookup"><span data-stu-id="7353c-103">LINEADDRESSMODE\_ Constants</span></span>

<span data-ttu-id="7353c-104">Le costanti del flag di bit **LINEADDRESSMODE \_** descrivono diversi modi per identificare un indirizzo in un dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="7353c-104">The **LINEADDRESSMODE\_** bit-flag constants describe various ways of identifying an address on a line device.</span></span>

<dl> <dt>

<span data-ttu-id="7353c-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**\_ADDRESSID LINEADDRESSMODE**</span><span class="sxs-lookup"><span data-stu-id="7353c-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE\_ADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7353c-106">L'indirizzo viene specificato con un numero intero piccolo nell'intervallo compreso tra 0 e *dwNumAddresses* meno uno, dove *dwNumAddresses* è il valore nelle funzionalità del dispositivo della riga.</span><span class="sxs-lookup"><span data-stu-id="7353c-106">The address is specified with a small integer in the range 0 to *dwNumAddresses* minus one, where *dwNumAddresses* is the value in the line's device capabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7353c-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**\_DIALABLEADDR LINEADDRESSMODE**</span><span class="sxs-lookup"><span data-stu-id="7353c-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE\_DIALABLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7353c-108">L'indirizzo viene specificato tramite il numero di telefono.</span><span class="sxs-lookup"><span data-stu-id="7353c-108">The address is specified through its phone number.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7353c-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="7353c-109">Remarks</span></span>

<span data-ttu-id="7353c-110">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7353c-110">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="7353c-111">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="7353c-111">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="7353c-112">Questa costante viene utilizzata per selezionare un indirizzo su una riga in cui viene originata una chiamata.</span><span class="sxs-lookup"><span data-stu-id="7353c-112">This constant is used to select an address on a line on which to originate a call.</span></span> <span data-ttu-id="7353c-113">Il modello usuale seleziona l'indirizzo per mezzo del relativo identificatore di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7353c-113">The usual model would select the address by means of its address identifier.</span></span> <span data-ttu-id="7353c-114">Gli identificatori di indirizzo sono il meccanismo usato per identificare gli indirizzi in TAPI.</span><span class="sxs-lookup"><span data-stu-id="7353c-114">Address identifiers are the mechanism used to identify addresses throughout TAPI.</span></span> <span data-ttu-id="7353c-115">Tuttavia, in alcuni ambienti, quando si effettua una chiamata, è spesso più pratico identificare l'indirizzo di origine di una chiamata in base al numero di telefono anziché all'identificatore dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7353c-115">However, in some environments, when making a call, it is often more practical to identify a call's originating address by phone number rather than by address identifier.</span></span> <span data-ttu-id="7353c-116">Un esempio è la possibile modellazione di un numero elevato di stazioni (di terze parti) nel compartimento per mezzo di un dispositivo a linee con molti indirizzi.</span><span class="sxs-lookup"><span data-stu-id="7353c-116">One example is in the possible modeling of large numbers of stations (third party) on the switch by means of one line device with many addresses.</span></span> <span data-ttu-id="7353c-117">La riga rappresenta il set di tutte le stazioni e ogni stazione viene mappata a un indirizzo con il proprio numero di telefono primario e identificatore di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7353c-117">The line represents the set of all stations, and each station is mapped to an address with its own primary phone number and address identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="7353c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7353c-118">Requirements</span></span>



| <span data-ttu-id="7353c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7353c-119">Requirement</span></span> | <span data-ttu-id="7353c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7353c-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7353c-121">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7353c-121">TAPI version</span></span><br/> | <span data-ttu-id="7353c-122">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7353c-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7353c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7353c-123">Header</span></span><br/>       | <dl> <span data-ttu-id="7353c-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7353c-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




