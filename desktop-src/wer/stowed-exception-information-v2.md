---
title: Struttura STOWED_EXCEPTION_INFORMATION_V2
description: Contiene informazioni sulle eccezioni riposte.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- Struttura STOWED_EXCEPTION_INFORMATION_V2 Segnalazione errori Windows
- Puntatore alla struttura PSTOWED_EXCEPTION_INFORMATION_V2 Segnalazione errori Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302378"
---
# <a name="stowed_exception_information_v2-structure"></a><span data-ttu-id="f8795-105">\_Struttura di informazioni sulle eccezioni riportate \_ \_ v2</span><span class="sxs-lookup"><span data-stu-id="f8795-105">STOWED\_EXCEPTION\_INFORMATION\_V2 structure</span></span>

<span data-ttu-id="f8795-106">Contiene informazioni sulle eccezioni riposte.</span><span class="sxs-lookup"><span data-stu-id="f8795-106">Contains stowed exception info.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8795-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8795-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a><span data-ttu-id="f8795-108">Members</span><span class="sxs-lookup"><span data-stu-id="f8795-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8795-109">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f8795-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-110">Tipo: **[ **\_ \_ \_ intestazione informazioni eccezione** riposte](stowed-exception-information-header.md)**</span><span class="sxs-lookup"><span data-stu-id="f8795-110">Type: **[**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-111">Struttura [**dell' \_ \_ \_ intestazione delle informazioni sull'eccezione**](stowed-exception-information-header.md) riposta che contiene informazioni per la struttura padre.</span><span class="sxs-lookup"><span data-stu-id="f8795-111">The [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) structure that contains info for this parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="f8795-112">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="f8795-112">**ResultCode**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-113">Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-113">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-114">Codice [**HRESULT**](/windows/desktop/WinProg/windows-data-types) per l'eccezione riposta.</span><span class="sxs-lookup"><span data-stu-id="f8795-114">The [**HRESULT**](/windows/desktop/WinProg/windows-data-types) code for the stowed exception.</span></span>

</dd> <dt>

<span data-ttu-id="f8795-115">**ExceptionForm**</span><span class="sxs-lookup"><span data-stu-id="f8795-115">**ExceptionForm**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-116">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-116">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-117">Valore a 2 bit che identifica il formato dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f8795-117">A 2-bit value that identifies the form of the exception.</span></span>



| <span data-ttu-id="f8795-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f8795-118">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="f8795-119">Significato</span><span class="sxs-lookup"><span data-stu-id="f8795-119">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <span data-ttu-id="f8795-120">Ricollocato <dt>**\_ Formato di eccezione 0x01 \_ \_ binario**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f8795-120"><dt>**STOWED\_EXCEPTION\_FORM\_BINARY**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="f8795-121">Questo valore indica che il formato dell'eccezione è binario.</span><span class="sxs-lookup"><span data-stu-id="f8795-121">This value indicates that the form of the exception is binary.</span></span><br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <span data-ttu-id="f8795-122">Ricollocato <dt>**\_ Formato dell'eccezione \_ \_ testo**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="f8795-122"><dt>**STOWED\_EXCEPTION\_FORM\_TEXT**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="f8795-123">Questo valore indica che il formato dell'eccezione è testo.</span><span class="sxs-lookup"><span data-stu-id="f8795-123">This value indicates that the form of the exception is text.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f8795-124">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="f8795-124">**ThreadId**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-125">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-125">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-126">Valore A 30 bit che identifica il thread che ha generato l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f8795-126">A 30-bit value that identifies the thread that raised the exception.</span></span> <span data-ttu-id="f8795-127">Il valore viene spostato a destra di 2 bit quando viene archiviato.</span><span class="sxs-lookup"><span data-stu-id="f8795-127">The value is shifted to the right by 2 bits when it's stored.</span></span> <span data-ttu-id="f8795-128">Per convertirlo di nuovo in un ID di thread valido, spostare il valore a sinistra di 2.</span><span class="sxs-lookup"><span data-stu-id="f8795-128">To convert it back to a valid thread ID, shift the value to the left by 2.</span></span> <span data-ttu-id="f8795-129">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f8795-129">For example:</span></span>

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

<span data-ttu-id="f8795-130">(*struct senza nome*)</span><span class="sxs-lookup"><span data-stu-id="f8795-130">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="f8795-131">I membri di questa struttura nidificata sono validi solo se il membro **ExceptionForm** è impostato **su \_ \_ \_ binary form Exception**.</span><span class="sxs-lookup"><span data-stu-id="f8795-131">The members of this nested structure are valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_BINARY**.</span></span>

<dl> <dt>

<span data-ttu-id="f8795-132">**ExceptionAddress**</span><span class="sxs-lookup"><span data-stu-id="f8795-132">**ExceptionAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-133">Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-133">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-134">Puntatore che contiene l'indirizzo dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f8795-134">A pointer that contains the exception address.</span></span>

</dd> <dt>

<span data-ttu-id="f8795-135">**StackTraceWordSize**</span><span class="sxs-lookup"><span data-stu-id="f8795-135">**StackTraceWordSize**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-136">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-136">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-137">Dimensione, in byte, di ogni parola nell'analisi dello stack a cui fa riferimento il membro **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="f8795-137">Size, in bytes, of each word in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="f8795-138">Questo valore è impostato su 4 per le piattaforme a 32 bit e 8 per le piattaforme a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f8795-138">This value is set to 4 for 32-bit platforms and 8 for 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="f8795-139">**StackTraceWords**</span><span class="sxs-lookup"><span data-stu-id="f8795-139">**StackTraceWords**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-140">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-140">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-141">Numero di parole nell'analisi dello stack a cui punta il membro **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="f8795-141">The number of words in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="f8795-142">Il numero di parole è uguale al numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="f8795-142">The number of words is equal to the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="f8795-143">**StackTrace**</span><span class="sxs-lookup"><span data-stu-id="f8795-143">**StackTrace**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-144">Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-144">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-145">Puntatore a un blocco di memoria che contiene l'analisi dello stack.</span><span class="sxs-lookup"><span data-stu-id="f8795-145">A pointer to a memory block that contains the stack trace.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f8795-146">(*struct senza nome*)</span><span class="sxs-lookup"><span data-stu-id="f8795-146">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="f8795-147">Il membro di questa struttura annidata è valido solo se il membro **ExceptionForm** è impostato per il **testo del \_ \_ form \_ dell'eccezione**.</span><span class="sxs-lookup"><span data-stu-id="f8795-147">The member of this nested structure is valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_TEXT**.</span></span>

<dl> <dt>

<span data-ttu-id="f8795-148">**ErrorText**</span><span class="sxs-lookup"><span data-stu-id="f8795-148">**ErrorText**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-149">Tipo: **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-149">Type: **[**PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-150">Puntatore a una stringa con terminazione null che contiene il testo dell'errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f8795-150">A pointer to a null-terminated string that contains the error text of the exception.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f8795-151">**NestedExceptionType**</span><span class="sxs-lookup"><span data-stu-id="f8795-151">**NestedExceptionType**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-152">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-152">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-153">Valore a 32 bit che specifica il tipo di oggetto a cui fa riferimento il membro **annidato** .</span><span class="sxs-lookup"><span data-stu-id="f8795-153">A 32-bit value that specifies the type of object that the **NestedException** member points to.</span></span> <span data-ttu-id="f8795-154">Definire il valore con questa macro di definizione del tipo di scambio di byte che presuppone little-endian:</span><span class="sxs-lookup"><span data-stu-id="f8795-154">Define the value with this byte swap type-definition macro that assumes little-endian:</span></span>

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

<span data-ttu-id="f8795-155">Di seguito sono riportate alcune definizioni di tipi comuni:</span><span class="sxs-lookup"><span data-stu-id="f8795-155">Here are some common type definitions:</span></span>



| <span data-ttu-id="f8795-156">Valore</span><span class="sxs-lookup"><span data-stu-id="f8795-156">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="f8795-157">Significato</span><span class="sxs-lookup"><span data-stu-id="f8795-157">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <span data-ttu-id="f8795-158">Ricollocato <dt>**\_ \_Tipo annidato eccezione \_ \_ None**</dt> <dt>(0x00000000)</dt></span><span class="sxs-lookup"><span data-stu-id="f8795-158"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_NONE**</dt> <dt>(0x00000000)</dt></span></span> </dl>                                  | <span data-ttu-id="f8795-159">Questo valore specifica che non è presente alcun oggetto eccezione annidato.</span><span class="sxs-lookup"><span data-stu-id="f8795-159">This value specifies that there is no nested exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <span data-ttu-id="f8795-160">Ricollocato <dt>**\_ Tipo \_ \_ \_**</dt> annidato eccezione tipo annidato Win32 <dt> \_ \_ \_ (' W32E ')</dt></span><span class="sxs-lookup"><span data-stu-id="f8795-160"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_WIN32**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('W32E')</dt></span></span> </dl>    | <span data-ttu-id="f8795-161">Questo valore specifica che il membro **annidato** fa riferimento a un oggetto [**\_ record di eccezione**](/windows/desktop/api/winnt/ns-winnt-exception_record) .</span><span class="sxs-lookup"><span data-stu-id="f8795-161">This value specifies that the **NestedException** member points to an [**EXCEPTION\_RECORD**](/windows/desktop/api/winnt/ns-winnt-exception_record) object.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <span data-ttu-id="f8795-162">Ricollocato <dt>**\_ tipo \_ \_ \_**</dt> annidato dell'eccezione ristivato del tipo annidato <dt> \_ \_ \_ (' Stow ')</dt></span><span class="sxs-lookup"><span data-stu-id="f8795-162"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_STOWED**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('STOW')</dt></span></span> </dl> | <span data-ttu-id="f8795-163">Questo valore specifica che il membro **annidato** fa riferimento a un altro oggetto eccezione stivata.</span><span class="sxs-lookup"><span data-stu-id="f8795-163">This value specifies that the **NestedException** member points to another stowed exception object.</span></span> <span data-ttu-id="f8795-164">L'altro oggetto eccezione riposta può essere un oggetto di **\_ \_ informazioni sulle \_ eccezioni** stivate o una versione diversa con un membro di **intestazione** valido, ovvero un membro di **intestazione** che contiene un' [**\_ \_ \_ intestazione di informazioni sull'eccezione**](stowed-exception-information-header.md)riposta valida.</span><span class="sxs-lookup"><span data-stu-id="f8795-164">The other stowed exception object can be a **STOWED\_EXCEPTION\_INFORMATION\_V2** object or a different version with a valid **Header** member, that is, a **Header** member that contains a valid [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md).</span></span><br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <span data-ttu-id="f8795-165">Ricollocato <dt>**\_ Tipo annidato eccezione \_ \_ \_ CLR**</dt> <dt>ristivato tipo annidato \_ \_ \_ (' nel clr1')</dt></span><span class="sxs-lookup"><span data-stu-id="f8795-165"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_CLR**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('CLR1')</dt></span></span> </dl>          | <span data-ttu-id="f8795-166">Questo valore specifica che il membro **annidato** fa riferimento a un oggetto eccezione ' nel clr1'.</span><span class="sxs-lookup"><span data-stu-id="f8795-166">This value specifies that the **NestedException** member points to a 'CLR1' exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <span data-ttu-id="f8795-167">Ricollocato <dt>**\_ Tipo \_ \_ \_**</dt> annidato eccezione tipo annidato eccezione Leo <dt>stivato \_ \_ \_ (' Leo1')</dt></span><span class="sxs-lookup"><span data-stu-id="f8795-167"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_LEO**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('LEO1')</dt></span></span> </dl>          | <span data-ttu-id="f8795-168">Questo valore specifica che il membro **annidato** fa riferimento a un oggetto eccezione della lingua.</span><span class="sxs-lookup"><span data-stu-id="f8795-168">This value specifies that the **NestedException** member points to a language exception object.</span></span><br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="f8795-169">**Annidaexception**</span><span class="sxs-lookup"><span data-stu-id="f8795-169">**NestedException**</span></span>
</dt> <dd>

<span data-ttu-id="f8795-170">Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8795-170">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f8795-171">Puntatore a un tipo di eccezione annidato.</span><span class="sxs-lookup"><span data-stu-id="f8795-171">A pointer to a nested exception type.</span></span> <span data-ttu-id="f8795-172">Il tipo di oggetto è indicato dal membro **NestedExceptionType** .</span><span class="sxs-lookup"><span data-stu-id="f8795-172">The type of object is indicated by the **NestedExceptionType** member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8795-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8795-173">Remarks</span></span>

<span data-ttu-id="f8795-174">Ricollocato **\_ \_Le informazioni sull'eccezione \_ v2** e l' [**\_ \_ \_ intestazione delle informazioni sulle eccezioni**](stowed-exception-information-header.md) riposte non sono attualmente definite in un'intestazione disponibile pubblicamente, pertanto è necessario definirle nel codice sorgente prima di utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="f8795-174">**STOWED\_EXCEPTION\_INFORMATION\_V2** and [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="f8795-175">La struttura di **\_ \_ informazioni \_ sull'eccezione ristivata** è identica a questa struttura, ad eccezione del fatto che non contiene i membri **NestedExceptionType** e **annidaexception** .</span><span class="sxs-lookup"><span data-stu-id="f8795-175">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8795-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8795-176">Requirements</span></span>



| <span data-ttu-id="f8795-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8795-177">Requirement</span></span> | <span data-ttu-id="f8795-178">Valore</span><span class="sxs-lookup"><span data-stu-id="f8795-178">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f8795-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8795-179">Minimum supported client</span></span><br/> | <span data-ttu-id="f8795-180">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8795-180">Windows 8.1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8795-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8795-181">Minimum supported server</span></span><br/> | <span data-ttu-id="f8795-182">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8795-182">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f8795-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8795-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8795-184"><dt>Nessuno</dt></span><span class="sxs-lookup"><span data-stu-id="f8795-184"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8795-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8795-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8795-186">**RECORD di eccezione \_**</span><span class="sxs-lookup"><span data-stu-id="f8795-186">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="f8795-187">**\_ \_ intestazione informazioni sulle eccezioni riposte \_**</span><span class="sxs-lookup"><span data-stu-id="f8795-187">**STOWED\_EXCEPTION\_INFORMATION\_HEADER**</span></span>](stowed-exception-information-header.md)
</dt> </dl>

 

