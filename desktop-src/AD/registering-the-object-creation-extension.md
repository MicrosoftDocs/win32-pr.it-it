---
title: Registrazione dell'estensione per la creazione di oggetti
description: Quando viene creata una DLL di estensione per la creazione di oggetti in Active Directory Domain Services, deve essere registrata nel registro di sistema di Windows e Active Directory Domain Services per rendere COM e gli snap-in di MMC amministrativi Active Directory a conoscenza dell'estensione.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956306"
---
# <a name="registering-the-object-creation-extension"></a><span data-ttu-id="4d649-103">Registrazione dell'estensione per la creazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="4d649-103">Registering the Object Creation Extension</span></span>

<span data-ttu-id="4d649-104">Quando viene creata una DLL di estensione per la creazione di oggetti in Active Directory Domain Services, deve essere registrata nel registro di sistema di Windows e Active Directory Domain Services per rendere COM e gli snap-in di MMC amministrativi Active Directory a conoscenza dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="4d649-104">When an object creation extension DLL in Active Directory Domain Services is created, it must be registered with the Windows registry and Active Directory Domain Services to make COM and the Active Directory administrative MMC snap-ins aware of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="4d649-105">Registrazione nel registro di sistema di Windows</span><span class="sxs-lookup"><span data-stu-id="4d649-105">Registering in the Windows Registry</span></span>

<span data-ttu-id="4d649-106">Come tutti i server COM, un'estensione per la creazione di oggetti deve essere registrata nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="4d649-106">Like all COM servers, an object creation extension must be registered in the Windows registry.</span></span> <span data-ttu-id="4d649-107">L'estensione viene registrata con la chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="4d649-107">The extension is registered under the following key:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

<span data-ttu-id="4d649-108">" &lt; estensione CLSID &gt; " è la rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="4d649-108">"&lt;extension CLSID&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="4d649-109">" &lt; percorso estensione &gt; " contiene il percorso e il nome file della DLL di estensione.</span><span class="sxs-lookup"><span data-stu-id="4d649-109">"&lt;extension path&gt;" contains the path and file name of the extension DLL.</span></span> <span data-ttu-id="4d649-110">Il valore **ThreadingModel** per tutte le estensioni per la creazione di oggetti deve essere "Apartment".</span><span class="sxs-lookup"><span data-stu-id="4d649-110">The **ThreadingModel** value for all object creation extensions must be "Apartment".</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="4d649-111">Registrazione con Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="4d649-111">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="4d649-112">La registrazione dell'estensione per la creazione di oggetti è specifica di un'impostazione locale.</span><span class="sxs-lookup"><span data-stu-id="4d649-112">Object creation extension registration is specific to one locale.</span></span> <span data-ttu-id="4d649-113">Se l'estensione per la creazione di oggetti si applica a tutte le impostazioni locali, deve essere registrata nell'oggetto **displaySpecifier** della classe di oggetti in tutti i sottocontenitori delle impostazioni locali nel contenitore DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="4d649-113">If the object creation extension applies to all locales, it must be registered in the object class's **displaySpecifier** object in all of the locale subcontainers in the DisplaySpecifiers container.</span></span> <span data-ttu-id="4d649-114">Se l'estensione per la creazione di oggetti è localizzata per determinate impostazioni locali, registrarla nell'oggetto **displaySpecifier** del sottocontenitore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="4d649-114">If the object creation extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="4d649-115">Per altre informazioni sul contenitore e sulle impostazioni locali di DisplaySpecifiers, vedere [identificatori di visualizzazione](display-specifiers.md) e [contenitore DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="4d649-115">For more information about the DisplaySpecifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="4d649-116">Sono disponibili due attributi DisplaySpecifier in cui è possibile registrare un'estensione per la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="4d649-116">There are two DisplaySpecifier attributes that an object creation extension can be registered under.</span></span> <span data-ttu-id="4d649-117">Si tratta di **creationWizard** e **createWizardExt**.</span><span class="sxs-lookup"><span data-stu-id="4d649-117">These are **creationWizard** and **createWizardExt**.</span></span>

<span data-ttu-id="4d649-118">L'attributo **creationWizard** identifica le estensioni per la creazione di oggetti primari per sostituire la creazione guidata oggetto esistente o nativa in Active Directory snap-in amministrativi. Un'estensione per la creazione primaria fornisce il primo set di pagine ed è ospitata in modo analogo alle pagine native.</span><span class="sxs-lookup"><span data-stu-id="4d649-118">The **creationWizard** attribute identifies primary object creation extensions to replace the existing or native object creation wizard in Active Directory administrative snap-ins. A primary creation extension provides the first set of pages and is hosted in the same way as native pages.</span></span> <span data-ttu-id="4d649-119">Questo attributo è a valore singolo e richiede il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="4d649-119">This attribute is single-valued and requires the following format:</span></span>


```C++
<CLSID>
```



<span data-ttu-id="4d649-120">" &lt; CLSID &gt; " è la rappresentazione di stringa del CLSID dell'oggetto com come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="4d649-120">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="4d649-121">L'attributo **createWizardExt** identifica le estensioni per la creazione di oggetti secondari.</span><span class="sxs-lookup"><span data-stu-id="4d649-121">The **createWizardExt** attribute identifies secondary object creation extensions.</span></span> <span data-ttu-id="4d649-122">Un'estensione per la creazione secondaria aggiunge le pagine della procedura guidata alle pagine native o all'estensione primaria.</span><span class="sxs-lookup"><span data-stu-id="4d649-122">A secondary creation extension adds wizard pages to the native pages or primary extension.</span></span> <span data-ttu-id="4d649-123">Questo attributo è multivalore e richiede il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="4d649-123">This attribute is multi-valued and requires the following format:</span></span>


```C++
<order number>,<CLSID>
```



<span data-ttu-id="4d649-124">Il " &lt; numero &gt; di ordine" è un numero senza segno che rappresenta la posizione della pagina nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="4d649-124">The "&lt;order number&gt;" is an unsigned number that represents the page's position in the wizard.</span></span> <span data-ttu-id="4d649-125">Quando viene visualizzata una procedura guidata di creazione, i valori vengono ordinati usando un confronto tra il " &lt; numero di ordine" di ogni valore &gt; .</span><span class="sxs-lookup"><span data-stu-id="4d649-125">When a creation wizard is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="4d649-126">Se più di un valore ha lo stesso " &lt; numero &gt; di ordine", le pagine vengono caricate nell'ordine in cui vengono lette dal server Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4d649-126">If more than one value has the same "&lt;order number&gt;", those pages are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="4d649-127">Se possibile, è consigliabile usare un " &lt; numero di ordine" non esistente, &gt; ovvero uno che non è stato usato da altri valori nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d649-127">If possible, you should use a non-existing "&lt;order number&gt;" (that is, one that has not been used by other values in the property).</span></span> <span data-ttu-id="4d649-128">Non esiste una posizione di inizio prescritta e sono consentiti gap nella &lt; sequenza "Order Number &gt; ".</span><span class="sxs-lookup"><span data-stu-id="4d649-128">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="4d649-129">" &lt; CLSID &gt; " è la rappresentazione di stringa del CLSID dell'oggetto com come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="4d649-129">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

 

 