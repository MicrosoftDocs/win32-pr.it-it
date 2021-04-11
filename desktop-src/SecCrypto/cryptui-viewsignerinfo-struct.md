---
description: Contiene informazioni per la funzione CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Struttura CRYPTUI_VIEWSIGNERINFO_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050008"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a><span data-ttu-id="43008-103">\_ \_ Struttura struct VIEWSIGNERINFO CRYPTUI</span><span class="sxs-lookup"><span data-stu-id="43008-103">CRYPTUI\_VIEWSIGNERINFO\_STRUCT structure</span></span>

<span data-ttu-id="43008-104">\[La struttura dello **\_ \_ struct VIEWSIGNERINFO CRYPTUI** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="43008-104">\[The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="43008-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="43008-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="43008-106">La struttura **CRYPTUI \_ VIEWSIGNERINFO \_ struct** contiene informazioni per la funzione [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="43008-106">The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure contains information for the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="43008-107">Questa struttura non è dichiarata in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="43008-107">This structure is not declared in a published header file.</span></span> <span data-ttu-id="43008-108">Per usare questa struttura, dichiararla nel formato esatto indicato.</span><span class="sxs-lookup"><span data-stu-id="43008-108">To use this structure, declare it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="43008-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43008-109">Syntax</span></span>


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a><span data-ttu-id="43008-110">Members</span><span class="sxs-lookup"><span data-stu-id="43008-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="43008-111">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="43008-111">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="43008-112">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="43008-112">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="43008-113">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="43008-113">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="43008-114">Handle della finestra che deve essere l'elemento padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="43008-114">The handle of the window to be the parent of the dialog box.</span></span> <span data-ttu-id="43008-115">Questo membro può essere **null** se la finestra di dialogo non deve avere un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="43008-115">This member can be **NULL** if the dialog box should have no parent.</span></span>

</dd> <dt>

<span data-ttu-id="43008-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="43008-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="43008-117">Set di flag che modifica il comportamento della funzione [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="43008-117">A set of flags that modifies the behavior of the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span> <span data-ttu-id="43008-118">Non sono attualmente definiti flag, pertanto il membro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="43008-118">There are no flags currently defined, so this member must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="43008-119">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="43008-119">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="43008-120">Puntatore a una stringa con terminazione null che contiene il titolo da visualizzare nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="43008-120">A pointer to a null-terminated string that contains the title to be displayed in the dialog box.</span></span> <span data-ttu-id="43008-121">Se questo membro è **null**, viene utilizzato un titolo predefinito.</span><span class="sxs-lookup"><span data-stu-id="43008-121">If this member is **NULL**, a default title is used.</span></span>

</dd> <dt>

<span data-ttu-id="43008-122">**pSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="43008-122">**pSignerInfo**</span></span>
</dt> <dd>

<span data-ttu-id="43008-123">Puntatore a una struttura [**di \_ \_ informazioni sul firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) che contiene le informazioni sul firmatario da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="43008-123">A pointer to a [**CMSG\_SIGNER\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) structure that contains the signer information to display.</span></span>

</dd> <dt>

<span data-ttu-id="43008-124">**hMsg**</span><span class="sxs-lookup"><span data-stu-id="43008-124">**hMsg**</span></span>
</dt> <dd>

<span data-ttu-id="43008-125">Handle del messaggio dal quale sono state estratte le informazioni sul firmatario.</span><span class="sxs-lookup"><span data-stu-id="43008-125">The handle of the message that the signer information was extracted from.</span></span>

</dd> <dt>

<span data-ttu-id="43008-126">**pszOID**</span><span class="sxs-lookup"><span data-stu-id="43008-126">**pszOID**</span></span>
</dt> <dd>

<span data-ttu-id="43008-127">Puntatore a una stringa ANSI con terminazione null che contiene la rappresentazione di stringa dell' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) che indica la convalida del certificato per cui è stata effettuata la firma.</span><span class="sxs-lookup"><span data-stu-id="43008-127">A pointer to a null-terminated ANSI string that contains the string representation of the [*object identifier*](../secgloss/o-gly.md) (OID) that signifies what the certificate that did the signing should be validated for.</span></span> <span data-ttu-id="43008-128">Se, ad esempio, viene chiamato il metodo per visualizzare la firma di un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL), è necessario passare la stringa OID di **\_ \_ \_ \_ firma utilizzo szOID KP CTL** .</span><span class="sxs-lookup"><span data-stu-id="43008-128">For example, if this is being called to view the signature of a [*certificate trust list*](../secgloss/c-gly.md) (CTL), the **szOID\_KP\_CTL\_USAGE\_SIGNING** OID string should be passed in.</span></span> <span data-ttu-id="43008-129">Se questo membro è **null**, il certificato non viene convalidato per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="43008-129">If this member is **NULL**, the certificate is not validated for usages.</span></span>

</dd> <dt>

<span data-ttu-id="43008-130">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="43008-130">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="43008-131">Questo parametro non è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="43008-131">This parameter is not currently used.</span></span> <span data-ttu-id="43008-132">Questo membro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="43008-132">This member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43008-133">**cStores**</span><span class="sxs-lookup"><span data-stu-id="43008-133">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="43008-134">Numero di elementi nella matrice **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="43008-134">The number of elements in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="43008-135">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="43008-135">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="43008-136">Matrice di valori **HCERTSTORE** che rappresentano gli altri archivi certificati in cui cercare il certificato che ha firmato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="43008-136">An array of **HCERTSTORE** values that represent the other certificate stores to search for the certificate that signed the message.</span></span> <span data-ttu-id="43008-137">Se questo membro è **null**, non viene eseguita la ricerca di altri archivi.</span><span class="sxs-lookup"><span data-stu-id="43008-137">If this member is **NULL**, no additional stores are searched.</span></span> <span data-ttu-id="43008-138">Il membro **cStores** contiene il numero di elementi in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="43008-138">The **cStores** member contains the number of elements in this array.</span></span>

</dd> <dt>

<span data-ttu-id="43008-139">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="43008-139">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="43008-140">Numero di elementi nella matrice **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="43008-140">The number of elements in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="43008-141">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="43008-141">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="43008-142">Matrice di puntatori della struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) che definiscono le pagine aggiuntive da visualizzare nella finestra di dialogo standard.</span><span class="sxs-lookup"><span data-stu-id="43008-142">An array of [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) structure pointers that define any extra pages to display in the standard dialog box.</span></span> <span data-ttu-id="43008-143">Se questo membro è **null**, non verrà visualizzata alcuna pagina aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="43008-143">If this member is **NULL**, no additional pages will be displayed.</span></span> <span data-ttu-id="43008-144">Il membro **cPropSheetPages** contiene il numero di elementi in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="43008-144">The **cPropSheetPages** member contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43008-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43008-145">Requirements</span></span>



| <span data-ttu-id="43008-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="43008-146">Requirement</span></span> | <span data-ttu-id="43008-147">Valore</span><span class="sxs-lookup"><span data-stu-id="43008-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43008-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43008-148">Minimum supported client</span></span><br/> | <span data-ttu-id="43008-149">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="43008-149">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="43008-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43008-150">Minimum supported server</span></span><br/> | <span data-ttu-id="43008-151">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43008-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="43008-152">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="43008-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="43008-153">**CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) e **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="43008-153">**CRYPTUI\_VIEWSIGNERINFO\_STRUCTW** (Unicode) and **CRYPTUI\_VIEWSIGNERINFO\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43008-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43008-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43008-155">**CryptUIDlgViewSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="43008-155">**CryptUIDlgViewSignerInfo**</span></span>](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
