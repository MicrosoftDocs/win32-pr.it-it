---
description: Converte un nome delle impostazioni locali in un identificatore delle impostazioni locali che può essere utilizzato per ottenere informazioni dal sistema operativo.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Funzione DownlevelLocaleNameToLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317159"
---
# <a name="downlevellocalenametolcid-function"></a><span data-ttu-id="31c5e-103">DownlevelLocaleNameToLCID (funzione)</span><span class="sxs-lookup"><span data-stu-id="31c5e-103">DownlevelLocaleNameToLCID function</span></span>

<span data-ttu-id="31c5e-104">Converte un [nome delle impostazioni locali](locale-names.md) in un [identificatore delle impostazioni locali](locale-identifiers.md) che può essere utilizzato per ottenere informazioni dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31c5e-104">Converts a [locale name](locale-names.md) to a [locale identifier](locale-identifiers.md) that can be used to get information from the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="31c5e-105">Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31c5e-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="31c5e-106">Il relativo utilizzo richiede un pacchetto di download.</span><span class="sxs-lookup"><span data-stu-id="31c5e-106">Its use requires a download package.</span></span> <span data-ttu-id="31c5e-107">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) per recuperare un identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="31c5e-107">Applications that only run on Windows Vista and later should call [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) to retrieve a locale identifier.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="31c5e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31c5e-108">Syntax</span></span>


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="31c5e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="31c5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c5e-110">*lpName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31c5e-110">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31c5e-111">Puntatore a una stringa con terminazione null che rappresenta il [nome delle impostazioni locali](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="31c5e-111">Pointer to a null-terminated string representing a [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="31c5e-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31c5e-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31c5e-113">Flag che specificano il tipo di nome.</span><span class="sxs-lookup"><span data-stu-id="31c5e-113">Flags specifying the type of name.</span></span> <span data-ttu-id="31c5e-114">Il valore predefinito è il \_ nome delle impostazioni locali di livello inferiore \_ .</span><span class="sxs-lookup"><span data-stu-id="31c5e-114">The default is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31c5e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31c5e-115">Return value</span></span>

<span data-ttu-id="31c5e-116">Restituisce l'identificatore delle impostazioni locali che corrisponde al nome delle impostazioni locali in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="31c5e-116">Returns the locale identifier that corresponds to the locale name if successful.</span></span>

<span data-ttu-id="31c5e-117">Se l'operazione non riesce, la funzione restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="31c5e-117">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="31c5e-118">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="31c5e-118">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="31c5e-119">flag di errore \_ non validi \_ .</span><span class="sxs-lookup"><span data-stu-id="31c5e-119">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="31c5e-120">I valori specificati per i flag non sono validi.</span><span class="sxs-lookup"><span data-stu-id="31c5e-120">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="31c5e-121">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="31c5e-121">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="31c5e-122">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="31c5e-122">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="31c5e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="31c5e-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="31c5e-124">Questa funzione non supporta le impostazioni locali non associate ad alcun paese.</span><span class="sxs-lookup"><span data-stu-id="31c5e-124">This function does not support neutral locales.</span></span> <span data-ttu-id="31c5e-125">La funzione [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) equivalente supporta [impostazioni locali personalizzate](custom-locales.md), ma solo per Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="31c5e-125">The equivalent [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function supports [custom locales](custom-locales.md), but only for Windows Vista and later.</span></span>

 

<span data-ttu-id="31c5e-126">Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="31c5e-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="31c5e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31c5e-127">Requirements</span></span>



| <span data-ttu-id="31c5e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="31c5e-128">Requirement</span></span> | <span data-ttu-id="31c5e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="31c5e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c5e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31c5e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="31c5e-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31c5e-131">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="31c5e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31c5e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="31c5e-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31c5e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="31c5e-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="31c5e-134">Redistributable</span></span><br/>          | <span data-ttu-id="31c5e-135">API di mapping dei dati di livello inferiore Microsoft NLS in Windows XP con SP2 e laterorWindows vista</span><span class="sxs-lookup"><span data-stu-id="31c5e-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="31c5e-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31c5e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c5e-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31c5e-137"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="31c5e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="31c5e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31c5e-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31c5e-139"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="31c5e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31c5e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c5e-141">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="31c5e-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="31c5e-142">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="31c5e-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="31c5e-143">Mapping dei dati delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="31c5e-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="31c5e-144">**LocaleNameToLCID**</span><span class="sxs-lookup"><span data-stu-id="31c5e-144">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
