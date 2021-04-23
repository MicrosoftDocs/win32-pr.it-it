---
description: Visualizza una finestra di dialogo che consente a un utente di selezionare un certificato.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Funzione CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 8f015796671990491407d91cbd51761816c5434b
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925692"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="649a7-103">Funzione CryptUIDlgSelectCertificate</span><span class="sxs-lookup"><span data-stu-id="649a7-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="649a7-104">La **funzione CryptUIDlgSelectCertificate** visualizza una finestra di dialogo che consente a un utente di selezionare un certificato.</span><span class="sxs-lookup"><span data-stu-id="649a7-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="649a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="649a7-105">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a><span data-ttu-id="649a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="649a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="649a7-107">*pcsc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="649a7-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649a7-108">Puntatore a una [**struttura \_ \_ STRUCT CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) che contiene informazioni sulla finestra di dialogo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="649a7-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="649a7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="649a7-109">Return value</span></span>

<span data-ttu-id="649a7-110">Puntatore a una [**struttura CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) che rappresenta il certificato selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="649a7-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="649a7-111">Al termine dell'uso di questo certificato, è necessario passare questo puntatore alla funzione [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) per decrementare il conteggio dei riferimenti del contesto del certificato.</span><span class="sxs-lookup"><span data-stu-id="649a7-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="649a7-112">Se il **membro dwFlags** della struttura *pcsc* non contiene il flag **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** un valore restituito **NULL** indica che l'utente ha chiuso la finestra di dialogo senza selezionare un certificato.</span><span class="sxs-lookup"><span data-stu-id="649a7-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="649a7-113">Se il **membro dwFlags** della *struttura pcsc* contiene il flag **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** questa funzione restituisce sempre **NULL.**</span><span class="sxs-lookup"><span data-stu-id="649a7-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="649a7-114">I certificati selezionati saranno contenuti nell'archivio certificati rappresentato dal membro **hSelectedCertStore** di *pcsc*.</span><span class="sxs-lookup"><span data-stu-id="649a7-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="649a7-115">Se il numero di certificati nell'archivio è lo stesso prima e dopo la chiamata di **CryptUIDlgSelectCertificate,** l'utente ha chiuso la finestra di dialogo senza selezionare alcun certificato.</span><span class="sxs-lookup"><span data-stu-id="649a7-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="649a7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="649a7-116">Remarks</span></span>

<span data-ttu-id="649a7-117">Se il **membro dwFlags** della struttura [**\_ \_ STRUCT CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) è impostato su **CRYPTUI \_ SELECTCERT \_ LEGACY,** viene visualizzata la finestra di dialogo legacy.</span><span class="sxs-lookup"><span data-stu-id="649a7-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="649a7-118">In caso contrario, viene visualizzata la finestra di dialogo di selezione del certificato corrente.</span><span class="sxs-lookup"><span data-stu-id="649a7-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="649a7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="649a7-119">Requirements</span></span>



| <span data-ttu-id="649a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="649a7-120">Requirement</span></span> | <span data-ttu-id="649a7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="649a7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="649a7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="649a7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="649a7-123">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="649a7-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="649a7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="649a7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="649a7-125">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="649a7-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="649a7-126">Fine del supporto</span><span class="sxs-lookup"><span data-stu-id="649a7-126">End of support</span></span><br/> | <span data-ttu-id="649a7-127">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="649a7-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="649a7-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="649a7-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="649a7-129"><dt>Cryptui.lib</dt></span><span class="sxs-lookup"><span data-stu-id="649a7-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="649a7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="649a7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="649a7-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="649a7-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="649a7-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="649a7-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="649a7-133">**CryptUIDlgSelectCertificateW** (Unicode) e **CryptUIDlgSelectCertificateA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="649a7-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="649a7-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="649a7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649a7-135">**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**</span><span class="sxs-lookup"><span data-stu-id="649a7-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>






