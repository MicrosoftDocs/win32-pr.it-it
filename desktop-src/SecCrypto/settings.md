---
description: Utilizzato per configurare i componenti di CAPICOM.
title: Oggetto Settings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330022"
---
# <a name="settings-object-cryptography"></a><span data-ttu-id="b12fe-103">Oggetto Settings (Cryptography)</span><span class="sxs-lookup"><span data-stu-id="b12fe-103">Settings object (Cryptography)</span></span>

<span data-ttu-id="b12fe-104">\[L'oggetto **Impostazioni** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="b12fe-104">\[The **Settings** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="b12fe-105">L'oggetto **Settings** viene usato per configurare i componenti di CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="b12fe-105">The **Settings** object is used to configure CAPICOM components.</span></span>

## <a name="members"></a><span data-ttu-id="b12fe-106">Membri</span><span class="sxs-lookup"><span data-stu-id="b12fe-106">Members</span></span>

<span data-ttu-id="b12fe-107">L'oggetto **Settings** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b12fe-107">The **Settings** object has these types of members:</span></span>

-   [<span data-ttu-id="b12fe-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b12fe-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b12fe-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b12fe-109">Properties</span></span>

<span data-ttu-id="b12fe-110">L'oggetto **Settings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b12fe-110">The **Settings** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b12fe-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b12fe-111">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b12fe-112">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="b12fe-112">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b12fe-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b12fe-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b12fe-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="b12fe-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b12fe-115">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b12fe-115">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b12fe-116">Imposta o Recupera il percorso di ricerca Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b12fe-116">Sets or retrieves the Active Directory search location.</span></span> <span data-ttu-id="b12fe-117">Per impostazione predefinita, la posizione iniziale non è specificata.</span><span class="sxs-lookup"><span data-stu-id="b12fe-117">The initial location is unspecified by default.</span></span> <span data-ttu-id="b12fe-118">Quando il percorso non è specificato, viene eseguita la ricerca nel catalogo globale, quindi viene eseguita la ricerca nel dominio predefinito.</span><span class="sxs-lookup"><span data-stu-id="b12fe-118">When the location is unspecified, the global catalog is searched, then the default domain is searched.</span></span> <span data-ttu-id="b12fe-119">La ricerca determina se l'attributo del certificato utente viene pubblicato in quel percorso.</span><span class="sxs-lookup"><span data-stu-id="b12fe-119">The search determines whether the user certificate attribute is published at that location.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b12fe-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="b12fe-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b12fe-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b12fe-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b12fe-122">Imposta o recupera un valore booleano che indica se è possibile utilizzare i prompt dell'interfaccia utente per l'identità di un firmatario o di un mittente.</span><span class="sxs-lookup"><span data-stu-id="b12fe-122">Sets or retrieves a Boolean value that indicates whether user interface prompts for a signer or sender's identity can be used.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b12fe-123">L'impostazione di questa proprietà non disabilita gli avvisi generati prima che l'utilizzo della chiave privata venga eseguito da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="b12fe-123">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b12fe-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="b12fe-124">Remarks</span></span>

<span data-ttu-id="b12fe-125">È possibile creare l'oggetto **Settings** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="b12fe-125">The **Settings** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b12fe-126">Il ProgID per l'oggetto **Settings** è capicom. Settings. 1.</span><span class="sxs-lookup"><span data-stu-id="b12fe-126">The ProgID for the **Settings** object is CAPICOM.Settings.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12fe-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b12fe-127">Requirements</span></span>



| <span data-ttu-id="b12fe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b12fe-128">Requirement</span></span> | <span data-ttu-id="b12fe-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b12fe-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b12fe-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b12fe-130">Redistributable</span></span><br/> | <span data-ttu-id="b12fe-131">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b12fe-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b12fe-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b12fe-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="b12fe-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b12fe-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b12fe-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b12fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b12fe-135">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="b12fe-135">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 




