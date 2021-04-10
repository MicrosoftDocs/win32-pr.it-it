---
title: funzione glCallLists (GL. h)
description: La funzione glCallLists esegue un elenco di elenchi di visualizzazione.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- funzione glCallLists OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964358"
---
# <a name="glcalllists-function"></a><span data-ttu-id="e04b3-104">glCallLists (funzione)</span><span class="sxs-lookup"><span data-stu-id="e04b3-104">glCallLists function</span></span>

<span data-ttu-id="e04b3-105">La funzione **glCallLists** esegue un elenco di elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-105">The **glCallLists** function executes a list of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04b3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e04b3-106">Syntax</span></span>


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a><span data-ttu-id="e04b3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e04b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e04b3-108">*n*</span><span class="sxs-lookup"><span data-stu-id="e04b3-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="e04b3-109">Numero di elenchi di visualizzazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="e04b3-109">The number of display lists to be executed.</span></span>

</dd> <dt>

<span data-ttu-id="e04b3-110">*type*</span><span class="sxs-lookup"><span data-stu-id="e04b3-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="e04b3-111">Tipo di valori negli *elenchi*.</span><span class="sxs-lookup"><span data-stu-id="e04b3-111">The type of values in *lists*.</span></span> <span data-ttu-id="e04b3-112">Vengono accettate le seguenti costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="e04b3-112">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="e04b3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e04b3-113">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="e04b3-114">Significato</span><span class="sxs-lookup"><span data-stu-id="e04b3-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="e04b3-115"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-115"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="e04b3-116">Il parametro *lists* viene considerato come una matrice di byte con segno, ognuno nell'intervallo compreso tra-128 e 127.</span><span class="sxs-lookup"><span data-stu-id="e04b3-116">The *lists* parameter is treated as an array of signed bytes, each in the range -128 through 127.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="e04b3-117"><dt>**\_byte senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-117"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="e04b3-118">Il parametro *lists* viene considerato come una matrice di byte senza segno, ognuno nell'intervallo compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e04b3-118">The *lists* parameter is treated as an array of unsigned bytes, each in the range 0 through 255.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="e04b3-119"><dt>**\_short GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-119"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="e04b3-120">Il parametro *lists* viene considerato come una matrice di interi con segno a 2 byte, ognuno nell'intervallo compreso tra-32768 e 32767.</span><span class="sxs-lookup"><span data-stu-id="e04b3-120">The *lists* parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="e04b3-121"><dt>**\_short senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-121"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="e04b3-122">Il parametro *lists* viene considerato come una matrice di interi senza segno a 2 byte, ognuno nell'intervallo compreso tra 0 e 65535.</span><span class="sxs-lookup"><span data-stu-id="e04b3-122">The *lists* parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="e04b3-123"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-123"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="e04b3-124">Il parametro *lists* viene considerato come una matrice di interi con segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="e04b3-124">The *lists* parameter is treated as an array of signed 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="e04b3-125"><dt>**GL \_ senza segno \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-125"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="e04b3-126">Il parametro *lists* viene considerato come una matrice di interi senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="e04b3-126">The *lists* parameter is treated as an array of unsigned 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="e04b3-127"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-127"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="e04b3-128">Il parametro *lists* viene considerato come una matrice di valori a virgola mobile a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="e04b3-128">The *lists* parameter is treated as an array of 4-byte, floating-point values.</span></span><br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <span data-ttu-id="e04b3-129"><dt>**GL \_ 2 \_ byte**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-129"><dt>**GL\_2\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="e04b3-130">Il parametro *lists* viene considerato come una matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="e04b3-130">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="e04b3-131">Ogni coppia di byte specifica un singolo nome di elenco visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e04b3-131">Each pair of bytes specifies a single display-list name.</span></span> <span data-ttu-id="e04b3-132">Il valore della coppia viene calcolato come 256 volte il valore senza segno del primo byte e il valore senza segno del secondo byte.</span><span class="sxs-lookup"><span data-stu-id="e04b3-132">The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.</span></span><br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <span data-ttu-id="e04b3-133"><dt>**GL \_ 3 \_ byte**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-133"><dt>**GL\_3\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="e04b3-134">Il parametro *lists* viene considerato come una matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="e04b3-134">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="e04b3-135">Ogni tripletta di byte specifica un singolo nome di elenco visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e04b3-135">Each triplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="e04b3-136">Il valore della terna viene calcolato come 65536 volte il valore senza segno del primo byte, più 256 volte il valore senza segno del secondo byte, più il valore senza segno del terzo byte.</span><span class="sxs-lookup"><span data-stu-id="e04b3-136">The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.</span></span><br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <span data-ttu-id="e04b3-137"><dt>**GL \_ 4 \_ byte**</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-137"><dt>**GL\_4\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="e04b3-138">Il parametro *lists* viene considerato come una matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="e04b3-138">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="e04b3-139">Ogni quadruplo di byte specifica un solo nome di elenco visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e04b3-139">Each quadruplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="e04b3-140">Il valore del quadruplo viene calcolato come 16777216 volte il valore senza segno del primo byte, più 65536 volte il valore senza segno del secondo byte, più 256 volte il valore senza segno del terzo byte, più il valore senza segno del quarto byte.</span><span class="sxs-lookup"><span data-stu-id="e04b3-140">The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e04b3-141">*elenchi*</span><span class="sxs-lookup"><span data-stu-id="e04b3-141">*lists*</span></span> 
</dt> <dd>

<span data-ttu-id="e04b3-142">Indirizzo di una matrice di offset del nome nell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-142">The address of an array of name offsets in the display list.</span></span> <span data-ttu-id="e04b3-143">Il tipo di puntatore è void perché gli offset possono essere byte, Shorts, int o float, a seconda del valore di *tipo*.</span><span class="sxs-lookup"><span data-stu-id="e04b3-143">The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e04b3-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e04b3-144">Return value</span></span>

<span data-ttu-id="e04b3-145">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e04b3-145">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04b3-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="e04b3-146">Remarks</span></span>

<span data-ttu-id="e04b3-147">La funzione **glCallLists** causa l'esecuzione di ogni elenco di visualizzazione nell'elenco di nomi passati come *elenchi* .</span><span class="sxs-lookup"><span data-stu-id="e04b3-147">The **glCallLists** function causes each display list in the list of names passed as *lists* to be executed.</span></span> <span data-ttu-id="e04b3-148">Di conseguenza, le funzioni salvate in ogni elenco di visualizzazione vengono eseguite in ordine, come se fossero chiamate senza usare un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-148">As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list.</span></span> <span data-ttu-id="e04b3-149">I nomi degli elenchi di visualizzazione che non sono stati definiti vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e04b3-149">Names of display lists that have not been defined are ignored.</span></span>

<span data-ttu-id="e04b3-150">La funzione **glCallLists** fornisce un mezzo efficace per l'esecuzione degli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-150">The **glCallLists** function provides an efficient means for executing display lists.</span></span> <span data-ttu-id="e04b3-151">Il parametro *n* specifica il numero di elenchi con diversi formati di nome (specificati dal parametro di *tipo* ) **glCallLists** executes.</span><span class="sxs-lookup"><span data-stu-id="e04b3-151">The *n* parameter specifies the number of lists with various name formats (specified by the *type* parameter) **glCallLists** executes.</span></span>

<span data-ttu-id="e04b3-152">L'elenco dei nomi degli elenchi di visualizzazione non è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e04b3-152">The list of display list names is not null-terminated.</span></span> <span data-ttu-id="e04b3-153">Viene invece *specificato il* numero di nomi che devono essere presi dagli *elenchi*.</span><span class="sxs-lookup"><span data-stu-id="e04b3-153">Rather, *n* specifies how many names are to be taken from *lists*.</span></span>

<span data-ttu-id="e04b3-154">La funzione [**glListBase**](gllistbase.md) rende disponibile un ulteriore livello di riferimento indiretto.</span><span class="sxs-lookup"><span data-stu-id="e04b3-154">The [**glListBase**](gllistbase.md) function makes an additional level of indirection available.</span></span> <span data-ttu-id="e04b3-155">La funzione **glListBase** specifica un offset senza segno aggiunto a ogni nome di elenco visualizzato specificato negli *elenchi* prima dell'esecuzione dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-155">The **glListBase** function specifies an unsigned offset that is added to each display list name specified in *lists* before that display list is executed.</span></span>

<span data-ttu-id="e04b3-156">La funzione **glCallLists** può essere visualizzata all'interno di un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-156">The **glCallLists** function can appear inside a display list.</span></span> <span data-ttu-id="e04b3-157">Per evitare la possibilità di una ricorsione infinita risultante da elenchi di visualizzazione che si richiamano, viene applicato un limite al livello di annidamento degli elenchi di visualizzazione durante l'esecuzione dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-157">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution.</span></span> <span data-ttu-id="e04b3-158">Questo limite deve essere almeno 64 e dipende dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="e04b3-158">This limit must be at least 64, and it depends on the implementation.</span></span>

<span data-ttu-id="e04b3-159">Lo stato OpenGL non viene salvato e ripristinato tramite una chiamata a **glCallLists**.</span><span class="sxs-lookup"><span data-stu-id="e04b3-159">The OpenGL state is not saved and restored across a call to **glCallLists**.</span></span> <span data-ttu-id="e04b3-160">Pertanto, le modifiche apportate allo stato OpenGL durante l'esecuzione degli elenchi di visualizzazione rimangono al termine dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e04b3-160">Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed.</span></span> <span data-ttu-id="e04b3-161">Usare [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md) per mantenere lo stato OpenGL tra le chiamate **glCallLists** .</span><span class="sxs-lookup"><span data-stu-id="e04b3-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md) to preserve the OpenGL state across **glCallLists** calls.</span></span>

<span data-ttu-id="e04b3-162">È possibile eseguire gli elenchi di visualizzazione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md), purché nell'elenco di visualizzazione siano incluse solo le funzioni consentite in questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="e04b3-162">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="e04b3-163">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glCallLists** :</span><span class="sxs-lookup"><span data-stu-id="e04b3-163">The following functions retrieve information related to the **glCallLists** function:</span></span>

<span data-ttu-id="e04b3-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con elenco GL \_ argomento \_ base</span><span class="sxs-lookup"><span data-stu-id="e04b3-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIST\_BASE</span></span>

<span data-ttu-id="e04b3-165">**glGet** con elenco di \_ \_ \_ nidificazione elenco massimo argomenti</span><span class="sxs-lookup"><span data-stu-id="e04b3-165">**glGet** with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="e04b3-166">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="e04b3-166">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="e04b3-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e04b3-167">Requirements</span></span>



| <span data-ttu-id="e04b3-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="e04b3-168">Requirement</span></span> | <span data-ttu-id="e04b3-169">Valore</span><span class="sxs-lookup"><span data-stu-id="e04b3-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e04b3-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e04b3-170">Minimum supported client</span></span><br/> | <span data-ttu-id="e04b3-171">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e04b3-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e04b3-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e04b3-172">Minimum supported server</span></span><br/> | <span data-ttu-id="e04b3-173">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e04b3-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e04b3-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e04b3-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="e04b3-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e04b3-176">Libreria</span><span class="sxs-lookup"><span data-stu-id="e04b3-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="e04b3-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e04b3-178">DLL</span><span class="sxs-lookup"><span data-stu-id="e04b3-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e04b3-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e04b3-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04b3-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e04b3-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04b3-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e04b3-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e04b3-182">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="e04b3-182">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="e04b3-183">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="e04b3-183">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="e04b3-184">**Remo**</span><span class="sxs-lookup"><span data-stu-id="e04b3-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e04b3-185">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="e04b3-185">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="e04b3-186">**glGet**</span><span class="sxs-lookup"><span data-stu-id="e04b3-186">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e04b3-187">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="e04b3-187">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="e04b3-188">**glListBase**</span><span class="sxs-lookup"><span data-stu-id="e04b3-188">**glListBase**</span></span>](gllistbase.md)
</dt> <dt>

[<span data-ttu-id="e04b3-189">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="e04b3-189">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="e04b3-190">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="e04b3-190">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="e04b3-191">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="e04b3-191">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="e04b3-192">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="e04b3-192">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="e04b3-193">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="e04b3-193">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





