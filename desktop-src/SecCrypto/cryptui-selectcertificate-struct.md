---
description: Contiene informazioni sulla finestra di dialogo visualizzata dalla funzione CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Struttura CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318247"
---
# <a name="cryptui_selectcertificate_struct-structure"></a><span data-ttu-id="b17ef-103">\_ \_ Struttura struct SELECTCERTIFICATE CRYPTUI</span><span class="sxs-lookup"><span data-stu-id="b17ef-103">CRYPTUI\_SELECTCERTIFICATE\_STRUCT structure</span></span>

<span data-ttu-id="b17ef-104">La struttura **CRYPTUI \_ SELECTCERTIFICATE \_ struct** contiene informazioni sulla finestra di dialogo visualizzata dalla funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="b17ef-104">The **CRYPTUI\_SELECTCERTIFICATE\_STRUCT** structure contains information about the dialog box displayed by the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b17ef-105">Syntax</span></span>


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a><span data-ttu-id="b17ef-106">Members</span><span class="sxs-lookup"><span data-stu-id="b17ef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b17ef-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b17ef-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-108">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="b17ef-108">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-109">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="b17ef-109">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-110">Handle della finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b17ef-110">The handle of the parent window of the dialog box.</span></span> <span data-ttu-id="b17ef-111">Se questo valore è **null**, la finestra padre è la finestra desktop predefinita.</span><span class="sxs-lookup"><span data-stu-id="b17ef-111">If this value is **NULL**, the parent window is the default desktop window.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b17ef-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-113">Specifica opzioni aggiuntive per la funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="b17ef-113">Specifies additional options for the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span> <span data-ttu-id="b17ef-114">Può essere zero o un **or** bit per bit dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b17ef-114">This can be zero or a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="b17ef-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b17ef-115">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="b17ef-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b17ef-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <span data-ttu-id="b17ef-117"><dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-117"><dt>**CRYPTUI\_SELECTCERT\_ADDFROMDS**</dt></span></span> </dl>                              | <span data-ttu-id="b17ef-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b17ef-118">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <span data-ttu-id="b17ef-119"><dt>**CRYPTUI \_ SELECTCERT \_ legacy**</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-119"><dt>**CRYPTUI\_SELECTCERT\_LEGACY**</dt></span></span> </dl>                                       | <span data-ttu-id="b17ef-120">Specifica che deve essere visualizzata la finestra di dialogo legacy.</span><span class="sxs-lookup"><span data-stu-id="b17ef-120">Specifies that the legacy dialog is to be displayed.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <span data-ttu-id="b17ef-121"><dt>**CRYPTUI \_ SELECTCERT \_ MultiSelect**</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-121"><dt>**CRYPTUI\_SELECTCERT\_MULTISELECT**</dt></span></span> </dl>                        | <span data-ttu-id="b17ef-122">Consente all'utente di selezionare più di un certificato nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b17ef-122">Allows the user to select more than one certificate in the dialog box.</span></span> <span data-ttu-id="b17ef-123">Se questo flag è impostato, la funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) restituisce sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="b17ef-123">If this flag is set, the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function always returns **NULL**.</span></span> <span data-ttu-id="b17ef-124">Il membro **hSelectedCertStore** di questa struttura deve contenere un handle per un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="b17ef-124">The **hSelectedCertStore** member of this structure must contain a handle to a certificate store.</span></span> <span data-ttu-id="b17ef-125">I certificati selezionati dall'utente verranno aggiunti a questo archivio.</span><span class="sxs-lookup"><span data-stu-id="b17ef-125">The certificates selected by the user will be added to this store.</span></span><br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <span data-ttu-id="b17ef-126"><dt>**CRYPTUI \_ SELECTCERT- \_ Inserisci \_ finestra \_ in primo piano**</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-126"><dt>**CRYPTUI\_SELECTCERT\_PUT\_WINDOW\_TOPMOST**</dt></span></span> </dl> | <span data-ttu-id="b17ef-127">Impone che l'interfaccia utente di crittografia sia la finestra superiore sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="b17ef-127">Forces the cryptography UI to be the top window on the screen.</span></span><br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="b17ef-128">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="b17ef-128">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-129">Titolo visualizzato per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b17ef-129">The display title for the dialog box.</span></span> <span data-ttu-id="b17ef-130">Se il valore di questo membro è **null**, viene usato il titolo predefinito "Select certificate".</span><span class="sxs-lookup"><span data-stu-id="b17ef-130">If the value of this member is **NULL**, the default title of "Select Certificate" is used.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-131">**dwDontUseColumn**</span><span class="sxs-lookup"><span data-stu-id="b17ef-131">**dwDontUseColumn**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-132">Flag che possono essere combinati per escludere le colonne della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b17ef-132">Flags that can be combined to exclude columns of the display.</span></span>



| <span data-ttu-id="b17ef-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b17ef-133">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="b17ef-134">Significato</span><span class="sxs-lookup"><span data-stu-id="b17ef-134">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <span data-ttu-id="b17ef-135"><dt>**CRYPTUI \_ Selezionare \_ la \_ colonna ISSUEDTO**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-135"><dt>**CRYPTUI\_SELECT\_ISSUEDTO\_COLUMN**</dt> <dt>1 (0x1)</dt></span></span> </dl>             | <span data-ttu-id="b17ef-136">Non visualizzare le informazioni **ISSUEDTO** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-136">Do not display **ISSUEDTO** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <span data-ttu-id="b17ef-137"><dt>**CRYPTUI \_ Selezionare \_ la \_ colonna ISSUEDBY**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-137"><dt>**CRYPTUI\_SELECT\_ISSUEDBY\_COLUMN**</dt> <dt>2 (0x2)</dt></span></span> </dl>             | <span data-ttu-id="b17ef-138">Non visualizzare le informazioni **ISSUEDBY** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-138">Do not display **ISSUEDBY** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <span data-ttu-id="b17ef-139"><dt>**CRYPTUI \_ Seleziona \_ INTENDEDUSE \_ colonna**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-139"><dt>**CRYPTUI\_SELECT\_INTENDEDUSE\_COLUMN**</dt> <dt>4 (0x4)</dt></span></span> </dl>    | <span data-ttu-id="b17ef-140">Non visualizzare le informazioni **IntendedUse** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-140">Do not display **IntendedUse** information.</span></span><br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <span data-ttu-id="b17ef-141"><dt>**CRYPTUI \_ Selezionare \_ FriendlyName \_ Column**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-141"><dt>**CRYPTUI\_SELECT\_FRIENDLYNAME\_COLUMN**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="b17ef-142">Non visualizzare le informazioni sul nome.</span><span class="sxs-lookup"><span data-stu-id="b17ef-142">Do not display name information.</span></span><br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <span data-ttu-id="b17ef-143"><dt>**CRYPTUI \_ Selezionare \_ la \_ colonna location**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-143"><dt>**CRYPTUI\_SELECT\_LOCATION\_COLUMN**</dt> <dt>16 (0x10)</dt></span></span> </dl>           | <span data-ttu-id="b17ef-144">Non visualizzare le informazioni sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="b17ef-144">Do not display location information.</span></span><br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <span data-ttu-id="b17ef-145"><dt>**CRYPTUI \_ Selezionare \_ la \_ colonna di scadenza**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="b17ef-145"><dt>**CRYPTUI\_SELECT\_EXPIRATION\_COLUMN**</dt> <dt>32 (0x20)</dt></span></span> </dl>     | <span data-ttu-id="b17ef-146">Non visualizzare le informazioni sulla scadenza.</span><span class="sxs-lookup"><span data-stu-id="b17ef-146">Do not display expiration information.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="b17ef-147">**szDisplayString**</span><span class="sxs-lookup"><span data-stu-id="b17ef-147">**szDisplayString**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-148">Testo visualizzato nella finestra di dialogo per indicare all'utente.</span><span class="sxs-lookup"><span data-stu-id="b17ef-148">Text that is displayed in the dialog box to instruct the user.</span></span> <span data-ttu-id="b17ef-149">Se il valore di questo membro è **null**, viene usata la stringa predefinita "selezionare un certificato che si vuole usare".</span><span class="sxs-lookup"><span data-stu-id="b17ef-149">If the value of this member is **NULL**, the default string "Select a certificate you want to use" is used.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-150">**pFilterCallback**</span><span class="sxs-lookup"><span data-stu-id="b17ef-150">**pFilterCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-151">Puntatore a una funzione di callback [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) che filtra i certificati visualizzati nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b17ef-151">A pointer to a [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) callback function that filters the certificates that are displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-152">**pDisplayCallback**</span><span class="sxs-lookup"><span data-stu-id="b17ef-152">**pDisplayCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-153">Puntatore a una funzione di callback [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) che Visualizza i certificati selezionati dall'utente per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b17ef-153">A pointer to a [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) callback function that displays certificates that the user selects to view.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-154">**pvCallbackData**</span><span class="sxs-lookup"><span data-stu-id="b17ef-154">**pvCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-155">Dati aggiuntivi passati alle funzioni di callback specificate dai membri **pFilterCallback** e **pDisplayCallback** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-155">Additional data that is passed to the callback functions specified by the **pFilterCallback** and **pDisplayCallback** members.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-156">**cDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="b17ef-156">**cDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-157">Numero di archivi certificati nella matrice **rghDisplayStores** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-157">The number of certificate stores in the **rghDisplayStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-158">**rghDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="b17ef-158">**rghDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-159">Puntatore a una matrice di archivi che contengono certificati disponibili per la selezione nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b17ef-159">A pointer to an array of stores that contain certificates available for selection in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-160">**cStores**</span><span class="sxs-lookup"><span data-stu-id="b17ef-160">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-161">Numero di archivi certificati nella matrice **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-161">The number of certificate stores in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-162">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="b17ef-162">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-163">Puntatore a una matrice di archivi certificati da cercare durante la compilazione di una catena di certificati e la verifica dell'attendibilità per i certificati visualizzati nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b17ef-163">A pointer to an array of certificate stores to search when building a certificate chain and verifying trust for the certificates displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-164">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="b17ef-164">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-165">Numero di pagine delle proprietà nella matrice **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-165">The number of property pages in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-166">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="b17ef-166">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-167">Puntatore a una matrice di strutture **PROPSHEETPAGE** che rappresentano le pagine di proprietà passate alla finestra di dialogo visualizzazione certificati quando viene selezionato un certificato per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b17ef-167">A pointer to an array of **PROPSHEETPAGE** structures that represent property pages that are passed to the certificate viewing dialog box when a certificate is selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="b17ef-168">**hSelectedCertStore**</span><span class="sxs-lookup"><span data-stu-id="b17ef-168">**hSelectedCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="b17ef-169">Handle per un archivio certificati creato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="b17ef-169">A handle to a certificate store created by the caller.</span></span> <span data-ttu-id="b17ef-170">I certificati selezionati dall'utente vengono aggiunti a questo archivio.</span><span class="sxs-lookup"><span data-stu-id="b17ef-170">The certificates selected by the user are added to this store.</span></span> <span data-ttu-id="b17ef-171">Se il numero di certificati in questo archivio è uguale prima e dopo la chiamata di [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), l'utente ha chiuso la finestra di dialogo senza selezionare alcun certificato.</span><span class="sxs-lookup"><span data-stu-id="b17ef-171">If the number of certificates in this store is the same before and after calling [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), the user closed the dialog box without selecting any certificates.</span></span>

<span data-ttu-id="b17ef-172">Questo membro non viene utilizzato se il membro **dwFlags** di questa struttura non contiene il flag **CRYPTUI \_ SELECTCERT \_ MultiSelect** .</span><span class="sxs-lookup"><span data-stu-id="b17ef-172">This member is not used if the **dwFlags** member of this structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b17ef-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b17ef-173">Requirements</span></span>



| <span data-ttu-id="b17ef-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17ef-174">Requirement</span></span> | <span data-ttu-id="b17ef-175">Valore</span><span class="sxs-lookup"><span data-stu-id="b17ef-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b17ef-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b17ef-176">Minimum supported client</span></span><br/> | <span data-ttu-id="b17ef-177">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b17ef-177">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="b17ef-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b17ef-178">Minimum supported server</span></span><br/> | <span data-ttu-id="b17ef-179">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b17ef-179">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b17ef-180">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b17ef-180">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b17ef-181">**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) e **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b17ef-181">**CRYPTUI\_SELECTCERTIFICATE\_STRUCTW** (Unicode) and **CRYPTUI\_SELECTCERTIFICATE\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b17ef-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b17ef-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17ef-183">**CryptUIDlgSelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="b17ef-183">**CryptUIDlgSelectCertificate**</span></span>](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




