---
description: Recupera il nome della classe e altre informazioni associate a un GUID specificato nel manifesto di un componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326205"
---
# <a name="sxslookupclrguid-function"></a><span data-ttu-id="89a26-103">SxsLookupClrGuid (funzione)</span><span class="sxs-lookup"><span data-stu-id="89a26-103">SxsLookupClrGuid function</span></span>

<span data-ttu-id="89a26-104">Recupera il nome della classe e altre informazioni associate a un GUID specificato nel manifesto di un componente.</span><span class="sxs-lookup"><span data-stu-id="89a26-104">Retrieves the class name and other information associated with a given GUID in a component's manifest.</span></span> <span data-ttu-id="89a26-105">Questa funzione viene utilizzata solo quando si implementa l'interoperabilità non gestita di basso livello nel .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="89a26-105">This function is used only when implementing low-level managed-unmanaged interoperability in the .NET Framework.</span></span> <span data-ttu-id="89a26-106">Per ulteriori informazioni sull'interoperabilità non gestita gestita, vedere l'argomento relativo all'interoperabilità con codice non gestito in .NET Framework SDK, nonché [le applicazioni isolate e gli assembly affiancati](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="89a26-106">For more information about managed-unmanaged interoperability, see "Interoperating with Unmanaged Code" in the .NET Framework SDK and also [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="89a26-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89a26-107">Syntax</span></span>


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="89a26-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89a26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89a26-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89a26-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89a26-110">Combinazione di zero o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="89a26-110">A combination of zero or more of the following flags.</span></span>



| <span data-ttu-id="89a26-111">Valore</span><span class="sxs-lookup"><span data-stu-id="89a26-111">Value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="89a26-112">Significato</span><span class="sxs-lookup"><span data-stu-id="89a26-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <span data-ttu-id="89a26-113"><dt>**SxS \_ Il \_ GUID CLR di ricerca \_ \_ Usa \_ ACTCTX**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="89a26-113"><dt>**SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX**</dt> <dt>0x00000001</dt></span></span> </dl>              | <span data-ttu-id="89a26-114">Se questo flag è impostato, il parametro *hActCtx* deve contenere un handle del contesto di attivazione restituito dalla funzione [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="89a26-114">If this flag is set, then the *hActCtx* parameter must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="89a26-115">Se questo flag non è impostato, il parametro *hActCtx* viene ignorato e **SxsLookupClrGuid** Cerca il contesto di attivazione attualmente attivo (la funzione [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) viene utilizzata per rendere attivo un contesto di attivazione).</span><span class="sxs-lookup"><span data-stu-id="89a26-115">If this flag is not set, the *hActCtx* parameter is ignored and **SxsLookupClrGuid** searches the activation context that is currently active (the [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) function is used to make an activation context active).</span></span><br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <span data-ttu-id="89a26-116"><dt>**SxS \_ RICERCA \_ del \_ GUID CLR \_ trova 0x00010000 \_ surrogato**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="89a26-116"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE**</dt> <dt>0x00010000</dt></span></span> </dl>  | <span data-ttu-id="89a26-117">Se questo flag è impostato, **SxsLookupClrGuid** Cerca un surrogato.</span><span class="sxs-lookup"><span data-stu-id="89a26-117">If this flag is set, **SxsLookupClrGuid** searches for a surrogate.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <span data-ttu-id="89a26-118"><dt>**SxS \_ RICERCA \_ CLR \_ GUID \_ trova \_ \_ classe CLR**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="89a26-118"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="89a26-119">Se questo flag è impostato, **SxsLookupClrGuid** cerca una classe.</span><span class="sxs-lookup"><span data-stu-id="89a26-119">If this flag is set, **SxsLookupClrGuid** searches for a class.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <span data-ttu-id="89a26-120"><dt>**SxS \_ Il \_ GUID CLR di ricerca \_ \_ trova \_ qualsiasi**</dt> <dt>0x00030000</dt></span><span class="sxs-lookup"><span data-stu-id="89a26-120"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_ANY**</dt> <dt>0x00030000</dt></span></span> </dl>                    | <span data-ttu-id="89a26-121">Si tratta di una combinazione del **\_ GUID CLR di ricerca SxS \_ \_ \_ Find \_ surrogate** e **SxS \_ Lookup \_ CLR \_ GUID trova flag di \_ \_ \_ classe CLR** ; se sono impostati entrambi, **SxsLookupClrGuid** Cerca un surrogato per primo e solo se non ne trova uno, quindi cerca una classe.</span><span class="sxs-lookup"><span data-stu-id="89a26-121">This is a combination of the **SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE** and **SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS** flags; if both are set, **SxsLookupClrGuid** searches for a surrogate first, and only if it does not find one, then searches for a class.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="89a26-122">*pClsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89a26-122">*pClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89a26-123">Puntatore al GUID su cui cercare le informazioni di interoperatività nel contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="89a26-123">A pointer to the GUID about which to search the activation context for interoperation information.</span></span> <span data-ttu-id="89a26-124">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="89a26-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="89a26-125">*hActCtx* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="89a26-125">*hActCtx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89a26-126">Se il **\_ GUID CLR di ricerca SxS usa il flag \_ \_ \_ \_ ACTCTX** è impostato nel parametro *dwFlags* , *hActCtx* deve contenere un handle del contesto di attivazione restituito dalla funzione [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="89a26-126">If the **SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX** flag is set in the *dwFlags* parameter, then *hActCtx* must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="89a26-127">In caso contrario, *hActCtx* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="89a26-127">Otherwise, *hActCtx* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="89a26-128">*pvOutputBuffer* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="89a26-128">*pvOutputBuffer* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89a26-129">Puntatore al buffer in cui vengono copiate le informazioni di restituzione.</span><span class="sxs-lookup"><span data-stu-id="89a26-129">Pointer to the buffer into which return information is copied.</span></span> <span data-ttu-id="89a26-130">Questo parametro può avere un valore NULL solo se il parametro *cbOutputBuffer* è con valore zero.</span><span class="sxs-lookup"><span data-stu-id="89a26-130">This parameter may be NULL-valued only if the *cbOutputBuffer* parameter is zero-valued.</span></span> <span data-ttu-id="89a26-131">I dati inseriti in questo buffer all'uscita (se presente) sono costituiti da una struttura **\_ \_ \_ CLR di informazioni GUID di SxS** seguita da eventuali dati stringa aggiuntivi necessari.</span><span class="sxs-lookup"><span data-stu-id="89a26-131">The data placed in this buffer on exit (if any) consists of a **SXS\_GUID\_INFORMATION\_CLR** structure followed by any additional string data required.</span></span> <span data-ttu-id="89a26-132">Per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="89a26-132">See the Remarks section below for more information.</span></span>

</dd> <dt>

<span data-ttu-id="89a26-133">*cbOutputBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89a26-133">*cbOutputBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89a26-134">Dimensioni in byte del buffer a cui punta il parametro *pvOutputBuffer* .</span><span class="sxs-lookup"><span data-stu-id="89a26-134">Size in bytes of the buffer pointed to by the *pvOutputBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="89a26-135">*pcbOutputBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89a26-135">*pcbOutputBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89a26-136">Puntatore a una variabile in cui la dimensione, in byte, delle informazioni restituite viene posizionata all'uscita.</span><span class="sxs-lookup"><span data-stu-id="89a26-136">Pointer to a variable where the size, in bytes, of the return information is placed on exit.</span></span> <span data-ttu-id="89a26-137">Se il parametro *cbOutputBuffer* è zero o se la dimensione del buffer di output è inferiore alla dimensione delle informazioni restituite, **SxsLookupClrGuid** ha esito negativo e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di **\_ \_ buffer insufficiente**.</span><span class="sxs-lookup"><span data-stu-id="89a26-137">If the *cbOutputBuffer* parameter is zero, or if the size of the output buffer is smaller than the size of the return information, then **SxsLookupClrGuid** fails and [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns an error of **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="89a26-138">In questo caso, usare il valore nella variabile a cui punta *pcbOutputBuffer* per allocare un buffer sufficientemente grande, quindi chiamare di nuovo **SxsLookupClrGuid** per recuperare le informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="89a26-138">In this case, use the value in the variable pointed to by *pcbOutputBuffer* to allocate a large enough buffer, and then call **SxsLookupClrGuid** again to retrieve the desired information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89a26-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89a26-139">Return value</span></span>

<span data-ttu-id="89a26-140">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="89a26-140">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="89a26-141">Per ulteriori informazioni sull'errore, chiamare [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="89a26-141">For more error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>

## <a name="remarks"></a><span data-ttu-id="89a26-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="89a26-142">Remarks</span></span>

<span data-ttu-id="89a26-143">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="89a26-143">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="89a26-144">I componenti gestiti possono dichiarare se stessi come supporto per gli assembly di interoperabilità gestiti, in modo da consentire a un consumer di componenti Win32 non gestito di fare riferimento all'assembly dichiarante.</span><span class="sxs-lookup"><span data-stu-id="89a26-144">Managed components may declare themselves as supporting managed "interop assemblies" so as to allow an unmanaged Win32 component consumer to reference the declaring assembly.</span></span> <span data-ttu-id="89a26-145">Il consumer di componenti può interagire con il componente gestito chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) su un GUID.</span><span class="sxs-lookup"><span data-stu-id="89a26-145">The component consumer can interact with the managed component by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on a GUID.</span></span> <span data-ttu-id="89a26-146">Il livello di interoperabilità instrada la richiesta di creazione dell'oggetto a .NET Framework, crea un'istanza dell'oggetto gestito e restituisce un puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="89a26-146">The interoperation layer routes the object creation request to .NET Framework, creates an instance of the managed object, and returns an interface pointer.</span></span>

<span data-ttu-id="89a26-147">**SxsLookupClrGuid** consente ai Framework di recuperare le informazioni associate a un determinato GUID nel manifesto del componente, ad esempio il nome della classe .NET, la versione del .NET Framework richiesta e l'assembly host in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="89a26-147">**SxsLookupClrGuid** allows the frameworks to retrieve information associated with a given GUID in the component's manifest, such as what its .NET class name is, what version of the .NET Framework it requires, and what host assembly it is located in.</span></span> <span data-ttu-id="89a26-148">I componenti gestiti pubblicano un assembly di interoperabilità contenente una serie di istruzioni che associano GUID a nomi di assembly e di tipi e i broker del runtime .NET la costruzione di istanze di oggetti gestiti quando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="89a26-148">Managed components publish an interop assembly that contains a number of statements associating GUIDs with assembly and type names, and the .NET runtime brokers the construction of managed object instances when [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is called.</span></span>

<span data-ttu-id="89a26-149">Di seguito è riportato un esempio di manifesto del componente che dichiara un GUID CLR e un surrogato CLR che **SxsLookupClrGuid** può cercare:</span><span class="sxs-lookup"><span data-stu-id="89a26-149">The following is a sample component manifest declaring a CLR GUID and a CLR surrogate that **SxsLookupClrGuid** can look up:</span></span>

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

<span data-ttu-id="89a26-150">Un provider di interoperabilità chiamerebbe **SxsLookupClrGuid** con un puntatore al GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" e riceverebbe in restituirà il nome della classe "MySampleSurrogate", la versione di runtime richiesta "1.0.3055" e l'identità testuale "DotNet. Sample. Surrogates, version =' 1.0.0.0', Type =' Interop '" del componente host.</span><span class="sxs-lookup"><span data-stu-id="89a26-150">An interoperation provider would call **SxsLookupClrGuid** with a pointer to the GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", and would receive in return the class name "MySampleSurrogate", the required runtime version "1.0.3055", and the textual identity "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" of the hosting component.</span></span>

<span data-ttu-id="89a26-151">Queste informazioni restituite sono contenute e/o a cui fa riferimento una struttura **\_ \_ \_ CLR di informazioni GUID di SxS** dichiarate come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="89a26-151">This return information would be contained and/or referenced by a **SXS\_GUID\_INFORMATION\_CLR** structure declared as follows.</span></span>

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

<span data-ttu-id="89a26-152">I membri di questa struttura contengono le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="89a26-152">The members of this structure contain the following information.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89a26-153">Membro</span><span class="sxs-lookup"><span data-stu-id="89a26-153">Member</span></span></th>
<th><span data-ttu-id="89a26-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89a26-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89a26-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span><span class="sxs-lookup"><span data-stu-id="89a26-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span></span><br/></td>
<td><span data-ttu-id="89a26-156">Contiene le dimensioni della struttura di SXS_GUID_INFORMATION_CLR (ciò consente di aumentare la struttura nelle versioni successive).</span><span class="sxs-lookup"><span data-stu-id="89a26-156">Contains the size of the SXS_GUID_INFORMATION_CLR structure (this allows the structure to grow in later versions).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89a26-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span><span class="sxs-lookup"><span data-stu-id="89a26-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span></span><br/></td>
<td><span data-ttu-id="89a26-158">Contiene uno dei due valori di flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="89a26-158">Contains one of the following two flag values:</span></span> <br/>
<ul>
<li><span data-ttu-id="89a26-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica che il GUID specificato è stato associato a un &quot; surrogato.&quot;</span><span class="sxs-lookup"><span data-stu-id="89a26-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Indicates that the specified GUID was associated with a &quot;surrogate.&quot;</span></span></li>
<li><span data-ttu-id="89a26-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica che il GUID specificato è stato associato a una &quot; classe.&quot;</span><span class="sxs-lookup"><span data-stu-id="89a26-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Indicates that the specified GUID was associated with a &quot;class.&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89a26-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span><span class="sxs-lookup"><span data-stu-id="89a26-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span></span><br/></td>
<td><span data-ttu-id="89a26-162">Punta a una stringa di caratteri wide con terminazione zero che identifica la versione del runtime specificata nel manifesto host per questa classe.</span><span class="sxs-lookup"><span data-stu-id="89a26-162">Points to a zero-terminated wide-character string that identifies the version of the runtime specified in the host manifest for this class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89a26-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="89a26-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span></span><br/></td>
<td><span data-ttu-id="89a26-164">Punta a una stringa di caratteri wide con terminazione zero che contiene il nome della classe .NET associata al GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="89a26-164">Points to a zero-terminated wide-character string that contains the name of the .NET class associated with the specified GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89a26-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="89a26-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span></span><br/></td>
<td><span data-ttu-id="89a26-166">Punta a una stringa di caratteri wide con terminazione zero che contiene l'identità testuale dell'assembly che ospita questa classe.</span><span class="sxs-lookup"><span data-stu-id="89a26-166">Points to a zero-terminated wide-character string that contains the textual identity of the assembly that hosts this class.</span></span> <span data-ttu-id="89a26-167">Per ulteriori informazioni sull'identità testuale, vedere &quot; specifica dei nomi di tipo completi in &quot; &quot; individuazione delle informazioni sul tipo in fase di esecuzione in &quot; &quot; programmazione con il .NET Framework &quot; in .NET Framework SDK.</span><span class="sxs-lookup"><span data-stu-id="89a26-167">For more information about textual identity, see &quot;Specifying Fully Qualified Type Names&quot; under &quot;Discovering Type Information at Run Time&quot; under &quot;Programming with the .NET Framework&quot; in the .NET Framework SDK.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="89a26-168">Un'applicazione non gestita può utilizzare le informazioni restituite in questo modo per caricare la versione corretta del .NET Framework, caricare l'assembly identificato dall'elemento **pcwszAssemblyIdentity** , quindi creare un'istanza della classe denominata dall'elemento **pcwszTypeName** .</span><span class="sxs-lookup"><span data-stu-id="89a26-168">An unmanaged application can use the information returned in this fashion to load the right version of the .NET Framework, load the assembly identified by the **pcwszAssemblyIdentity** element, and then create an instance of the class named by the **pcwszTypeName** element.</span></span>

## <a name="examples"></a><span data-ttu-id="89a26-169">Esempio</span><span class="sxs-lookup"><span data-stu-id="89a26-169">Examples</span></span>

<span data-ttu-id="89a26-170">Utilizzare il collegamento dinamico come indicato di seguito per chiamare la funzione **SxsLookupClrGuid** :</span><span class="sxs-lookup"><span data-stu-id="89a26-170">Use dynamic linking as follows to call the **SxsLookupClrGuid** function:</span></span>


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a><span data-ttu-id="89a26-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89a26-171">Requirements</span></span>



| <span data-ttu-id="89a26-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="89a26-172">Requirement</span></span> | <span data-ttu-id="89a26-173">Valore</span><span class="sxs-lookup"><span data-stu-id="89a26-173">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a26-174">DLL</span><span class="sxs-lookup"><span data-stu-id="89a26-174">DLL</span></span><br/> | <dl> <span data-ttu-id="89a26-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a26-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89a26-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89a26-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a26-177">Applicazioni isolate e assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="89a26-177">Isolated Applications and Side-by-side Assemblies</span></span>](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[<span data-ttu-id="89a26-178">**CreateActCtx**</span><span class="sxs-lookup"><span data-stu-id="89a26-178">**CreateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[<span data-ttu-id="89a26-179">**ActivateActCtx**</span><span class="sxs-lookup"><span data-stu-id="89a26-179">**ActivateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[<span data-ttu-id="89a26-180">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="89a26-180">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
