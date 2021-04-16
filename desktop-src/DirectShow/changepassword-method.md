---
description: Il metodo DVDAdm. ChangePassword salva una nuova password dell'applicazione nel registro di sistema.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword (metodo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481029"
---
# <a name="changepassword-method"></a><span data-ttu-id="7fb25-103">ChangePassword (metodo)</span><span class="sxs-lookup"><span data-stu-id="7fb25-103">ChangePassword Method</span></span>

> [!Note]  
> <span data-ttu-id="7fb25-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7fb25-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7fb25-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="7fb25-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7fb25-106">Il `DVDAdm.ChangePassword` metodo salva una nuova password dell'applicazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7fb25-106">The `DVDAdm.ChangePassword` method saves a new application password in the registry.</span></span>

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a><span data-ttu-id="7fb25-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fb25-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fb25-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="7fb25-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="7fb25-109">Specifica il nome di accesso dell'utente corrente sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="7fb25-109">Specifies the current user's logon name as a String.</span></span> <span data-ttu-id="7fb25-110">Il parametro viene ignorato dall'oggetto MSDVDAdm.</span><span class="sxs-lookup"><span data-stu-id="7fb25-110">The MSDVDAdm object ignores this parameter.</span></span> <span data-ttu-id="7fb25-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7fb25-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7fb25-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Venduti*</span><span class="sxs-lookup"><span data-stu-id="7fb25-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*sOld*</span></span>
</dt> <dd>

<span data-ttu-id="7fb25-113">Specifica la vecchia password dell'utente sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="7fb25-113">Specifies the user's old password as a String.</span></span>

</dd> <dt>

<span data-ttu-id="7fb25-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span><span class="sxs-lookup"><span data-stu-id="7fb25-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span></span>
</dt> <dd>

<span data-ttu-id="7fb25-115">Specifica la nuova password dell'utente sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="7fb25-115">Specifies the user's new password as a String.</span></span> <span data-ttu-id="7fb25-116">Non può essere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="7fb25-116">Cannot be an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fb25-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fb25-117">Return Value</span></span>

<span data-ttu-id="7fb25-118">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7fb25-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fb25-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fb25-119">Remarks</span></span>

<span data-ttu-id="7fb25-120">Attualmente, il parametro *sUserName* viene ignorato in questo e in tutti i metodi correlati.</span><span class="sxs-lookup"><span data-stu-id="7fb25-120">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span> <span data-ttu-id="7fb25-121">Ciò significa che chiunque conosca la password può impostare il livello padre.</span><span class="sxs-lookup"><span data-stu-id="7fb25-121">This means that whoever knows the password can set the parental level.</span></span> <span data-ttu-id="7fb25-122">Sono disponibili solo una password e un livello parentale per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fb25-122">There is only one password and one parental level for the application.</span></span> <span data-ttu-id="7fb25-123">Non è disponibile alcun supporto per i nomi di accesso utente singoli o per la gestione di più password.</span><span class="sxs-lookup"><span data-stu-id="7fb25-123">There is no support for individual user logon names or multiple password management.</span></span> <span data-ttu-id="7fb25-124">Per applicare i livelli di gestione padre, i genitori devono impostare la password e quindi impostare il livello padre appropriato per i membri più giovani del gruppo di parenti.</span><span class="sxs-lookup"><span data-stu-id="7fb25-124">To enforce parental management levels, parents should set the password and then set the parental level appropriate for younger members of the group of relatives.</span></span> <span data-ttu-id="7fb25-125">Quando i genitori vogliono visualizzare un disco con contenuto con classificazione adulta, possono modificare il livello e quindi modificarlo di nuovo al termine della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7fb25-125">When parents want to view a disc with adult-rated content, they can change the level, and then change it back when they are done viewing.</span></span> <span data-ttu-id="7fb25-126">Finché gli elementi figlio non conoscono la password, possono solo controllare il contenuto al di sotto del livello impostato.</span><span class="sxs-lookup"><span data-stu-id="7fb25-126">As long as the children do not know the password, they can only watch content at or below the level set for them.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fb25-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fb25-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb25-128">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="7fb25-128">**ConfirmPassword**</span></span>](confirmpassword-method.md)
</dt> <dt>

[<span data-ttu-id="7fb25-129">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="7fb25-129">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



