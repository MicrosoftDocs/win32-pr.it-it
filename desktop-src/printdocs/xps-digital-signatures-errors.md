---
description: Nella tabella seguente sono elencati tutti i valori HRESULT che possono essere restituiti dai metodi nell'API per la firma digitale XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Errori dell'API firma digitale XPS (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348211"
---
# <a name="xps-digital-signature-api-errors"></a><span data-ttu-id="9af80-103">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="9af80-103">XPS Digital Signature API Errors</span></span>

<span data-ttu-id="9af80-104">Nella tabella seguente sono elencati tutti i valori **HRESULT** che possono essere restituiti dai metodi nell'API per la firma digitale XPS.</span><span class="sxs-lookup"><span data-stu-id="9af80-104">The following table lists all **HRESULT** values that can be returned by the methods in the XPS Digital Signature API.</span></span> <span data-ttu-id="9af80-105">Si noti che non tutti i metodi possono restituire tutti i valori restituiti elencati in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="9af80-105">Note that not every method can return every return value listed in this table.</span></span>



| <span data-ttu-id="9af80-106">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="9af80-106">Return code/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="9af80-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9af80-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="9af80-108"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-108"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                                                                                 | <span data-ttu-id="9af80-109">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9af80-109">The method succeeded.</span></span><br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <span data-ttu-id="9af80-110"><dt>**XPS \_ E \_ \_ SIGNATUREBLOCK \_ markup 0x8052038b non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9af80-110"><dt>**XPS\_E\_INVALID\_SIGNATUREBLOCK\_MARKUP**</dt> <dt>0x8052038b</dt></span></span> </dl> | <span data-ttu-id="9af80-111">Si è verificato un errore nel markup XML del blocco della firma durante la lettura del markup della firma.</span><span class="sxs-lookup"><span data-stu-id="9af80-111">Encountered an error in the XML markup of the signature block while the signature markup was being read.</span></span><br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <span data-ttu-id="9af80-112"><dt>**XPS \_ \_Elementi di \_ compatibilità \_ del markup E**</dt> <dt>0x80520389</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-112"><dt>**XPS\_E\_MARKUP\_COMPATIBILITY\_ELEMENTS**</dt> <dt>0x80520389</dt></span></span> </dl> | <span data-ttu-id="9af80-113">Il valore dei [**\_ \_ flag di firma XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) ha specificato che non sono previsti elementi di compatibilità del markup. sono stati tuttavia trovati elementi di compatibilità del markup.</span><span class="sxs-lookup"><span data-stu-id="9af80-113">The [**XPS\_SIGN\_FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) value specified that no markup compatibility elements were expected; however, markup compatibility elements were found.</span></span><br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <span data-ttu-id="9af80-114"><dt>**XPS \_ E \_ oggetto \_ scollegato**</dt> <dt>0x8052038a</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-114"><dt>**XPS\_E\_OBJECT\_DETACHED**</dt> <dt>0x8052038a</dt></span></span> </dl>                                            | <span data-ttu-id="9af80-115">L'interfaccia non è associata alla gestione della firma.</span><span class="sxs-lookup"><span data-stu-id="9af80-115">The interface is not associated with the signature manager.</span></span><br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <span data-ttu-id="9af80-116"><dt>**XPS \_ Pacchetto di E \_ \_ già \_ aperto**</dt> <dt>0x80520387</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-116"><dt>**XPS\_E\_PACKAGE\_ALREADY\_OPENED**</dt> <dt>0x80520387</dt></span></span> </dl>                      | <span data-ttu-id="9af80-117">Un pacchetto XPS è già stato aperto in gestione firme.</span><span class="sxs-lookup"><span data-stu-id="9af80-117">An XPS package has already been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <span data-ttu-id="9af80-118"><dt>**XPS \_ \_Pacchetto E \_ non \_ aperto**</dt> <dt>0x80520386</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-118"><dt>**XPS\_E\_PACKAGE\_NOT\_OPENED**</dt> <dt>0x80520386</dt></span></span> </dl>                                  | <span data-ttu-id="9af80-119">Un pacchetto XPS non è ancora stato aperto in gestione firme.</span><span class="sxs-lookup"><span data-stu-id="9af80-119">An XPS package has not yet been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <span data-ttu-id="9af80-120"><dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-120"><dt>**XPS\_E\_SIGNATUREID\_DUP**</dt> <dt>0x80520388</dt></span></span> </dl>                                            | <span data-ttu-id="9af80-121">Due o più firme hanno lo stesso ID.</span><span class="sxs-lookup"><span data-stu-id="9af80-121">Two or more signatures have the same ID.</span></span><br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <span data-ttu-id="9af80-122"><dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-122"><dt>**XPS\_E\_SIGREQUESTID\_DUP**</dt> <dt>0x80520385</dt></span></span> </dl>                                         | <span data-ttu-id="9af80-123">L'ID richiesta di firma non è univoco all'interno del blocco della firma.</span><span class="sxs-lookup"><span data-stu-id="9af80-123">The signature request ID is not unique within the signature block.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="9af80-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9af80-124">Remarks</span></span>

<span data-ttu-id="9af80-125">Alcuni metodi API per la firma digitale XPS effettuano chiamate all'API di creazione dei [pacchetti](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="9af80-125">Some XPS digital signature API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="9af80-126">Per informazioni sui valori restituiti dell'API di creazione pacchetti, vedere errori di creazione [pacchetti](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="9af80-126">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="9af80-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9af80-127">Requirements</span></span>



| <span data-ttu-id="9af80-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af80-128">Requirement</span></span> | <span data-ttu-id="9af80-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9af80-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af80-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9af80-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9af80-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9af80-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="9af80-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9af80-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9af80-133">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9af80-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9af80-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9af80-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af80-135"><dt>XpsDigitalSignature. h</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-135"><dt>Xpsdigitalsignature.h</dt></span></span> </dl>   |
| <span data-ttu-id="9af80-136">IDL</span><span class="sxs-lookup"><span data-stu-id="9af80-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9af80-137"><dt>XpsDigitalSignature. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-137"><dt>XpsDigitalSignature.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af80-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9af80-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af80-139">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="9af80-139">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="9af80-140">Errori di creazione pacchetto</span><span class="sxs-lookup"><span data-stu-id="9af80-140">Packaging Errors</span></span>](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[<span data-ttu-id="9af80-141">Valori restituiti della crittografia</span><span class="sxs-lookup"><span data-stu-id="9af80-141">Cryptography Return Values</span></span>](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

