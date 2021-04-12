---
description: Recupera l'identificatore delle impostazioni locali per l'elemento padre delle impostazioni locali specificate.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Funzione DownlevelGetParentLocaleLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348146"
---
# <a name="downlevelgetparentlocalelcid-function"></a><span data-ttu-id="f86c8-103">DownlevelGetParentLocaleLCID (funzione)</span><span class="sxs-lookup"><span data-stu-id="f86c8-103">DownlevelGetParentLocaleLCID function</span></span>

<span data-ttu-id="f86c8-104">Recupera l' [identificatore delle impostazioni locali](locale-identifiers.md) per l'elemento padre delle impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="f86c8-104">Retrieves the [locale identifier](locale-identifiers.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="f86c8-105">Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f86c8-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="f86c8-106">Il relativo utilizzo richiede il pacchetto di download.</span><span class="sxs-lookup"><span data-stu-id="f86c8-106">Its use requires the download package.</span></span> <span data-ttu-id="f86c8-107">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [locale \_ SPARENT](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="f86c8-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f86c8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f86c8-108">Syntax</span></span>


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a><span data-ttu-id="f86c8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f86c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f86c8-110">*Impostazioni locali* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f86c8-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f86c8-111">Identificatore delle impostazioni locali per il quale recuperare l'identificatore delle impostazioni locali padre.</span><span class="sxs-lookup"><span data-stu-id="f86c8-111">Locale identifier of the locale for which to retrieve the parent locale identifier.</span></span> <span data-ttu-id="f86c8-112">È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali o usare uno dei valori predefiniti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f86c8-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="f86c8-113">impostazioni locali \_ INvariabili</span><span class="sxs-lookup"><span data-stu-id="f86c8-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="f86c8-114">impostazioni locali del \_ sistema \_</span><span class="sxs-lookup"><span data-stu-id="f86c8-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="f86c8-115">\_impostazione predefinita utente impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="f86c8-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="f86c8-116">**Windows Vista e versioni successive:** Sono supportati anche gli identificatori delle impostazioni locali personalizzati seguenti.</span><span class="sxs-lookup"><span data-stu-id="f86c8-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="f86c8-117">impostazioni locali \_ personalizzate \_ predefinite</span><span class="sxs-lookup"><span data-stu-id="f86c8-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="f86c8-118">\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="f86c8-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="f86c8-119">impostazioni locali \_ personalizzate non \_ specificate</span><span class="sxs-lookup"><span data-stu-id="f86c8-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f86c8-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f86c8-120">Return value</span></span>

<span data-ttu-id="f86c8-121">Restituisce l'identificatore delle impostazioni locali padre in caso di esito positivo; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="f86c8-121">Returns the parent locale identifier if successful, or 0 otherwise.</span></span> <span data-ttu-id="f86c8-122">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="f86c8-122">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="f86c8-123">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="f86c8-123">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="f86c8-124">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="f86c8-124">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f86c8-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f86c8-125">Remarks</span></span>

<span data-ttu-id="f86c8-126">Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="f86c8-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="f86c8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f86c8-127">Requirements</span></span>



| <span data-ttu-id="f86c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f86c8-128">Requirement</span></span> | <span data-ttu-id="f86c8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f86c8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f86c8-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f86c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f86c8-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f86c8-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f86c8-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f86c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f86c8-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f86c8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f86c8-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f86c8-134">Redistributable</span></span><br/>          | <span data-ttu-id="f86c8-135">API di mapping dei dati di livello inferiore Microsoft NLS XPor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f86c8-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XPor Windows Vista</span></span><br/>     |
| <span data-ttu-id="f86c8-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f86c8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f86c8-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f86c8-137"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="f86c8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f86c8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f86c8-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f86c8-139"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f86c8-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f86c8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86c8-141">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="f86c8-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f86c8-142">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="f86c8-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="f86c8-143">Mapping dei dati delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="f86c8-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="f86c8-144">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="f86c8-144">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
