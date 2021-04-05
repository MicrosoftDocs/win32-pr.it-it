---
description: Recupera il nome delle impostazioni locali per l'elemento padre delle impostazioni locali specificate.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Funzione DownlevelGetParentLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968320"
---
# <a name="downlevelgetparentlocalename-function"></a><span data-ttu-id="29043-103">DownlevelGetParentLocaleName (funzione)</span><span class="sxs-lookup"><span data-stu-id="29043-103">DownlevelGetParentLocaleName function</span></span>

<span data-ttu-id="29043-104">Recupera il [nome delle impostazioni locali](locale-names.md) per l'elemento padre delle impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="29043-104">Retrieves the [locale name](locale-names.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="29043-105">Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="29043-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="29043-106">Il relativo utilizzo richiede il pacchetto di download.</span><span class="sxs-lookup"><span data-stu-id="29043-106">Its use requires the download package.</span></span> <span data-ttu-id="29043-107">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [locale \_ SPARENT](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="29043-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="29043-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29043-108">Syntax</span></span>


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a><span data-ttu-id="29043-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="29043-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29043-110">*Impostazioni locali* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29043-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29043-111">[Identificatore](locale-identifiers.md) delle impostazioni locali delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="29043-111">[Locale identifier](locale-identifiers.md) of the locale.</span></span> <span data-ttu-id="29043-112">È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali o usare uno dei valori predefiniti seguenti.</span><span class="sxs-lookup"><span data-stu-id="29043-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="29043-113">impostazioni locali \_ INvariabili</span><span class="sxs-lookup"><span data-stu-id="29043-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="29043-114">impostazioni locali del \_ sistema \_</span><span class="sxs-lookup"><span data-stu-id="29043-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="29043-115">\_impostazione predefinita utente impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="29043-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="29043-116">**Windows Vista e versioni successive:** Sono supportati anche gli identificatori delle impostazioni locali personalizzati seguenti.</span><span class="sxs-lookup"><span data-stu-id="29043-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="29043-117">impostazioni locali \_ personalizzate \_ predefinite</span><span class="sxs-lookup"><span data-stu-id="29043-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="29043-118">\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="29043-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="29043-119">impostazioni locali \_ personalizzate non \_ specificate</span><span class="sxs-lookup"><span data-stu-id="29043-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="29043-120">*lpName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="29043-120">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29043-121">Puntatore a un buffer in cui la funzione recupera il nome delle impostazioni locali padre o uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="29043-121">Pointer to a buffer in which the function retrieves the parent locale name, or one of the following predefined values.</span></span> <span data-ttu-id="29043-122">Questo parametro è impostato su **null** se *cchName* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="29043-122">This parameter is set to **NULL** if *cchName* is set to 0.</span></span>

-   [<span data-ttu-id="29043-123">nome delle impostazioni locali \_ \_ invariante</span><span class="sxs-lookup"><span data-stu-id="29043-123">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="29043-124">impostazioni locali \_ nome \_ sistema \_ predefinito</span><span class="sxs-lookup"><span data-stu-id="29043-124">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="29043-125">\_ \_ impostazione predefinita utente nome impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="29043-125">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="29043-126">*cchName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29043-126">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29043-127">Dimensioni del buffer indicato da *lpName*, in punti di codice UTF-16.</span><span class="sxs-lookup"><span data-stu-id="29043-127">Size of the buffer indicated by *lpName*, in UTF-16 code points.</span></span> <span data-ttu-id="29043-128">Il valore 0 per questo parametro fa in modo che la funzione ignori il buffer *lpName* e restituisca la dimensione del buffer, in caratteri (caratteri null inclusi), necessaria per contenere il nome delle impostazioni locali padre.</span><span class="sxs-lookup"><span data-stu-id="29043-128">A value of 0 for this parameter causes the function to ignore the *lpName* buffer and return the size of the buffer, in characters (null characters included), required to contain the parent locale name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29043-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29043-129">Return value</span></span>

<span data-ttu-id="29043-130">Restituisce il numero di punti di codice UTF-16 nel nome delle impostazioni locali, incluso il carattere null di terminazione, in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="29043-130">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span>

<span data-ttu-id="29043-131">Questa funzione restituisce 0 in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="29043-131">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="29043-132">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="29043-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="29043-133">ERRORE \_ \_ nel buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="29043-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="29043-134">Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.</span><span class="sxs-lookup"><span data-stu-id="29043-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="29043-135">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="29043-135">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="29043-136">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="29043-136">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="29043-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="29043-137">Remarks</span></span>

<span data-ttu-id="29043-138">Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="29043-138">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="29043-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29043-139">Requirements</span></span>



| <span data-ttu-id="29043-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="29043-140">Requirement</span></span> | <span data-ttu-id="29043-141">Valore</span><span class="sxs-lookup"><span data-stu-id="29043-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29043-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29043-142">Minimum supported client</span></span><br/> | <span data-ttu-id="29043-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="29043-143">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="29043-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29043-144">Minimum supported server</span></span><br/> | <span data-ttu-id="29043-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29043-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29043-146">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="29043-146">Redistributable</span></span><br/>          | <span data-ttu-id="29043-147">API di mapping dei dati di livello inferiore Microsoft NLS in Windows XP con SP2 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="29043-147">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and later</span></span><br/>  |
| <span data-ttu-id="29043-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29043-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="29043-149"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="29043-149"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="29043-150">DLL</span><span class="sxs-lookup"><span data-stu-id="29043-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29043-151"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29043-151"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29043-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29043-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29043-153">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="29043-153">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="29043-154">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="29043-154">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="29043-155">Mapping dei dati delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="29043-155">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="29043-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="29043-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
