---
description: Le \_ costanti del flag di bit PHONEBUTTONMODE descrivono le classi di pulsanti.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: Costanti PHONEBUTTONMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4ee5e9835b7df06773bc1429641c91597c15e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333956"
---
# <a name="phonebuttonmode_-constants"></a><span data-ttu-id="7a066-103">\_Costanti PHONEBUTTONMODE</span><span class="sxs-lookup"><span data-stu-id="7a066-103">PHONEBUTTONMODE\_ Constants</span></span>

<span data-ttu-id="7a066-104">Le costanti del flag di bit **PHONEBUTTONMODE \_** descrivono le classi di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="7a066-104">The **PHONEBUTTONMODE\_** bit-flag constants describe the button classes.</span></span>

<dl> <dt>

<span data-ttu-id="7a066-105"><span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**\_chiamata PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="7a066-105"><span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**PHONEBUTTONMODE\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a066-106">Il pulsante viene assegnato a un aspetto della chiamata.</span><span class="sxs-lookup"><span data-stu-id="7a066-106">The button is assigned to a call appearance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a066-107"><span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**\_visualizzazione PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="7a066-107"><span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**PHONEBUTTONMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a066-108">Il pulsante è un pulsante "soft" associato alla visualizzazione del telefono.</span><span class="sxs-lookup"><span data-stu-id="7a066-108">The button is a "soft" button associated with the phone's display.</span></span> <span data-ttu-id="7a066-109">Un set di telefono può contenere zero o più pulsanti di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7a066-109">A phone set can have zero or more display buttons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a066-110"><span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**\_manichino PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="7a066-110"><span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE\_DUMMY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a066-111">Questo valore viene usato per descrivere la posizione di un pulsante o di una lampada senza pulsante corrispondente ma con solo una lampada.</span><span class="sxs-lookup"><span data-stu-id="7a066-111">This value is used to describe a button/lamp position that has no corresponding button but has only a lamp.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a066-112"><span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**\_funzionalità PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="7a066-112"><span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**PHONEBUTTONMODE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a066-113">Il pulsante viene assegnato alle funzionalità richieste dal commutatore, ad esempio attesa, conferenza e trasferimento.</span><span class="sxs-lookup"><span data-stu-id="7a066-113">The button is assigned to requesting features from the switch, such as hold, conference, and transfer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a066-114"><span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**\_tastiera PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="7a066-114"><span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**PHONEBUTTONMODE\_KEYPAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a066-115">Il pulsante è uno dei dodici pulsanti del tastierino, compreso tra 0 e 9,' \* ' è \# '.</span><span class="sxs-lookup"><span data-stu-id="7a066-115">The button is one of the twelve keypad buttons, 0 through 9, '\*', and '\#'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a066-116"><span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ locale**</span><span class="sxs-lookup"><span data-stu-id="7a066-116"><span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a066-117">Il pulsante è un pulsante della funzione locale, ad esempio mute o controllo volume.</span><span class="sxs-lookup"><span data-stu-id="7a066-117">The button is a local function button, such as mute or volume control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a066-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a066-118">Remarks</span></span>

<span data-ttu-id="7a066-119">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="7a066-119">No extensibility.</span></span> <span data-ttu-id="7a066-120">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="7a066-120">All 32 bits are reserved.</span></span>

<span data-ttu-id="7a066-121">Questo tipo di enumerazione viene utilizzato nella struttura dei dati [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) per descrivere il significato associato ai pulsanti del telefono.</span><span class="sxs-lookup"><span data-stu-id="7a066-121">This enumeration type is used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to describe the meaning associated with the phone's buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a066-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a066-122">Requirements</span></span>



| <span data-ttu-id="7a066-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a066-123">Requirement</span></span> | <span data-ttu-id="7a066-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7a066-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7a066-125">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7a066-125">TAPI version</span></span><br/> | <span data-ttu-id="7a066-126">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7a066-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7a066-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a066-127">Header</span></span><br/>       | <dl> <span data-ttu-id="7a066-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a066-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




