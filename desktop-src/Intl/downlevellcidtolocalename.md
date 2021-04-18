---
description: Converte un identificatore delle impostazioni locali in un nome delle impostazioni locali.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Funzione DownlevelLCIDToLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317162"
---
# <a name="downlevellcidtolocalename-function"></a><span data-ttu-id="bafd6-103">DownlevelLCIDToLocaleName (funzione)</span><span class="sxs-lookup"><span data-stu-id="bafd6-103">DownlevelLCIDToLocaleName function</span></span>

<span data-ttu-id="bafd6-104">Converte un [identificatore delle impostazioni locali](locale-identifiers.md) in un [nome delle impostazioni locali](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="bafd6-104">Converts a [locale identifier](locale-identifiers.md) to a [locale name](locale-names.md).</span></span>

> [!Note]  
> <span data-ttu-id="bafd6-105">Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bafd6-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="bafd6-106">Il relativo utilizzo richiede un pacchetto di download.</span><span class="sxs-lookup"><span data-stu-id="bafd6-106">Its use requires a download package.</span></span> <span data-ttu-id="bafd6-107">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) per recuperare un nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bafd6-107">Applications that run only on Windows Vista and later should call [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to retrieve a locale name.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bafd6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bafd6-108">Syntax</span></span>


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bafd6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bafd6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bafd6-110">*Impostazioni locali* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bafd6-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafd6-111">Identificatore delle impostazioni locali da tradurre.</span><span class="sxs-lookup"><span data-stu-id="bafd6-111">The locale identifier to translate.</span></span> <span data-ttu-id="bafd6-112">È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bafd6-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier.</span></span> <span data-ttu-id="bafd6-113">Questa funzione non supporta le impostazioni locali non associate ad alcun paese o i seguenti valori specifici dell'identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bafd6-113">This function does not support neutral locales or the following specific locale identifier values.</span></span>

-   [<span data-ttu-id="bafd6-114">impostazioni locali del \_ sistema \_</span><span class="sxs-lookup"><span data-stu-id="bafd6-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="bafd6-115">\_impostazione predefinita utente impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="bafd6-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)
-   [<span data-ttu-id="bafd6-116">impostazioni locali \_ personalizzate \_ predefinite</span><span class="sxs-lookup"><span data-stu-id="bafd6-116">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="bafd6-117">\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="bafd6-117">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="bafd6-118">impostazioni locali \_ personalizzate non \_ specificate</span><span class="sxs-lookup"><span data-stu-id="bafd6-118">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="bafd6-119">*lpName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bafd6-119">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafd6-120">Puntatore a un buffer in cui questa funzione recupera il nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bafd6-120">Pointer to a buffer in which this function retrieves the locale name.</span></span> <span data-ttu-id="bafd6-121">La funzione recupera **null** se *cchName* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="bafd6-121">The function retrieves **NULL** if *cchName* is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="bafd6-122">*cchName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bafd6-122">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafd6-123">Dimensioni, in punti di codice UTF-16, del buffer del nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bafd6-123">Size, in UTF-16 code points, of the locale name buffer.</span></span> <span data-ttu-id="bafd6-124">L'applicazione imposta questo parametro su 0 per restituire la dimensione richiesta del buffer del nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bafd6-124">The application sets this parameter to 0 to return the required size of the locale name buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bafd6-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bafd6-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafd6-126">Flag che specificano il tipo di nome da recuperare.</span><span class="sxs-lookup"><span data-stu-id="bafd6-126">Flags specifying the type of name to retrieve.</span></span> <span data-ttu-id="bafd6-127">Il valore predefinito è il \_ nome delle impostazioni locali di livello inferiore \_ .</span><span class="sxs-lookup"><span data-stu-id="bafd6-127">The default value is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bafd6-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bafd6-128">Return value</span></span>

<span data-ttu-id="bafd6-129">Restituisce il numero di punti di codice UTF-16 nel nome delle impostazioni locali, incluso il carattere null di terminazione, in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bafd6-129">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span> <span data-ttu-id="bafd6-130">Se la funzione ha esito positivo e il valore di *cchName* è 0, il valore restituito è la dimensione richiesta, in caratteri (compresi i caratteri null), per il buffer del nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bafd6-130">If the function succeeds and the value of *cchName* is 0, the return value is the required size, in characters (including null characters), for the locale name buffer.</span></span>

<span data-ttu-id="bafd6-131">Se l'operazione non riesce, la funzione restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="bafd6-131">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="bafd6-132">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="bafd6-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="bafd6-133">ERRORE \_ \_ nel buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="bafd6-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="bafd6-134">Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.</span><span class="sxs-lookup"><span data-stu-id="bafd6-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="bafd6-135">flag di errore \_ non validi \_ .</span><span class="sxs-lookup"><span data-stu-id="bafd6-135">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="bafd6-136">Il valore di *dwFlags* non è valido.</span><span class="sxs-lookup"><span data-stu-id="bafd6-136">The value of *dwFlags* is not valid.</span></span>
-   <span data-ttu-id="bafd6-137">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="bafd6-137">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="bafd6-138">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="bafd6-138">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="bafd6-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="bafd6-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bafd6-140">Questa funzione non supporta [impostazioni locali personalizzate](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="bafd6-140">This function does not support [custom locales](custom-locales.md).</span></span>

 

<span data-ttu-id="bafd6-141">Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="bafd6-141">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="bafd6-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bafd6-142">Requirements</span></span>



| <span data-ttu-id="bafd6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="bafd6-143">Requirement</span></span> | <span data-ttu-id="bafd6-144">Valore</span><span class="sxs-lookup"><span data-stu-id="bafd6-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bafd6-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bafd6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bafd6-146">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bafd6-146">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="bafd6-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bafd6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bafd6-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bafd6-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bafd6-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bafd6-149">Redistributable</span></span><br/>          | <span data-ttu-id="bafd6-150">API di mapping dei dati di livello inferiore Microsoft NLS in Windows XP con SP2 e laterorWindows vista</span><span class="sxs-lookup"><span data-stu-id="bafd6-150">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="bafd6-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bafd6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bafd6-152"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bafd6-152"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="bafd6-153">DLL</span><span class="sxs-lookup"><span data-stu-id="bafd6-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bafd6-154"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bafd6-154"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bafd6-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bafd6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafd6-156">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="bafd6-156">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="bafd6-157">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="bafd6-157">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="bafd6-158">Mapping dei dati delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="bafd6-158">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="bafd6-159">**LCIDToLocaleName**</span><span class="sxs-lookup"><span data-stu-id="bafd6-159">**LCIDToLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
