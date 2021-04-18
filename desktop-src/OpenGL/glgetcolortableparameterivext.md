---
title: funzione glGetColorTableParameterivEXT (GL. h)
description: Le funzioni glGetColorTableParameterfvEXT e glGetColorTableParameterivEXT ottengono i parametri della tavolozza dalle tabelle dei colori. | funzione glGetColorTableParameterivEXT (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- funzione glGetColorTableParameterivEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321798"
---
# <a name="glgetcolortableparameterivext-function"></a><span data-ttu-id="a08e7-105">glGetColorTableParameterivEXT (funzione)</span><span class="sxs-lookup"><span data-stu-id="a08e7-105">glGetColorTableParameterivEXT function</span></span>

<span data-ttu-id="a08e7-106">Le funzioni [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) e **glGetColorTableParameterivEXT** ottengono i parametri della tavolozza dalle tabelle dei colori.</span><span class="sxs-lookup"><span data-stu-id="a08e7-106">The [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) and **glGetColorTableParameterivEXT** functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08e7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a08e7-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="a08e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a08e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08e7-109">*target*</span><span class="sxs-lookup"><span data-stu-id="a08e7-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a08e7-110">Trama di destinazione della tavolozza per cui si desiderano i dati dei parametri.</span><span class="sxs-lookup"><span data-stu-id="a08e7-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="a08e7-111">Deve essere una trama \_ 1D, una trama \_ 2D, una \_ trama proxy \_ 1D o una trama del proxy \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="a08e7-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="a08e7-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="a08e7-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="a08e7-113">Costante simbolica per il *tipo di dati* del parametro della tavolozza a cui puntano i parametri.</span><span class="sxs-lookup"><span data-stu-id="a08e7-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="a08e7-114">Di seguito sono riportate le costanti simboliche accettate e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="a08e7-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="a08e7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a08e7-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="a08e7-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a08e7-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="a08e7-117"><dt>**\_ \_ formato tabella colori \_ GL \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e7-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="a08e7-118">Restituisce il formato interno specificato dalla chiamata più recente a [**glColorTableEXT**](glcolortableext.md) o il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a08e7-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="a08e7-119"><dt>**\_ \_ Larghezza tabella colori \_ GL \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e7-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="a08e7-120">Restituisce la larghezza della tavolozza corrente.</span><span class="sxs-lookup"><span data-stu-id="a08e7-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="a08e7-121"><dt>**\_ \_ \_ dimensioni rosse tabella colori \_ GL \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e7-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="a08e7-122">Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente rosso dei dati della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="a08e7-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="a08e7-123"><dt>**\_ \_ \_ dimensioni verdi tabella colore \_ GL \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e7-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="a08e7-124">Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente verde dei dati della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="a08e7-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="a08e7-125"><dt>**\_ \_ \_ dimensioni blu tabella colori \_ GL \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e7-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="a08e7-126">Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente blu dei dati della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="a08e7-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="a08e7-127"><dt>**\_ \_ \_ dimensioni alfa tabella colori \_ GL \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e7-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="a08e7-128">Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente alfa dei dati della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="a08e7-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="a08e7-129">*params*</span><span class="sxs-lookup"><span data-stu-id="a08e7-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a08e7-130">Punta ai dati dei parametri della tabella dei colori specificati dal parametro *pname* .</span><span class="sxs-lookup"><span data-stu-id="a08e7-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08e7-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a08e7-131">Return value</span></span>

<span data-ttu-id="a08e7-132">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a08e7-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08e7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="a08e7-133">Remarks</span></span>

<span data-ttu-id="a08e7-134">Usare le funzioni **glGetColorTableParameterivEXT** e [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) per recuperare dati di parametri specifici dalle tabelle dei colori impostate con [**glColorTableEXT**](glcolortableext.md) per le tavolozze delle trame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a08e7-134">You use the **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="a08e7-135">È anche possibile usare queste funzioni per determinare il numero di voci della tabella dei colori restituite da **glGetColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="a08e7-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="a08e7-136">Quando il parametro di *destinazione* è GL \_ proxy \_ texture \_ 1D o \_ GL proxy \_ texture \_ 2D e l'implementazione non supporta i valori specificati per il *formato* o la *larghezza*, **glColorTableEXT** può non essere in grado di creare la tabella dei colori richiesta.</span><span class="sxs-lookup"><span data-stu-id="a08e7-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="a08e7-137">In questo caso, la tabella dei colori è vuota e tutti i parametri recuperati saranno pari a zero.</span><span class="sxs-lookup"><span data-stu-id="a08e7-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="a08e7-138">È possibile determinare se OpenGL supporta un formato e una dimensione della tabella dei colori specifici chiamando **glColorTableEXT** con una destinazione proxy e quindi chiamando **glGetColorTableParameterivEXT** o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) per determinare se il parametro width corrisponde a quello impostato da **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="a08e7-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="a08e7-139">Se la larghezza recuperata è zero, la richiesta della tabella dei colori di **glColorTable** non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="a08e7-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="a08e7-140">Se la larghezza recuperata è diversa da zero, è possibile chiamare **glColorTable** con la destinazione reale con trama \_ 1D o trama \_ 2D per impostare la tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="a08e7-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="a08e7-141">Le funzioni **glGetColorTableParameterivEXT** e [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) sono funzioni di estensione che non fanno parte della libreria OpenGL standard, ma che fanno parte dell' \_ estensione di trama GL ext \_ tavolozza \_ .</span><span class="sxs-lookup"><span data-stu-id="a08e7-141">The **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="a08e7-142">Per verificare se l'implementazione di OpenGL supporta **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT**, chiamare [**glGetString**](glgetstring.md)**(** GL \_ Extensions **)**.</span><span class="sxs-lookup"><span data-stu-id="a08e7-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="a08e7-143">Se restituisce la \_ trama della \_ tavolozza GL ext \_ , **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** sono supportati.</span><span class="sxs-lookup"><span data-stu-id="a08e7-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="a08e7-144">Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="a08e7-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="a08e7-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a08e7-145">Requirements</span></span>



| <span data-ttu-id="a08e7-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a08e7-146">Requirement</span></span> | <span data-ttu-id="a08e7-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a08e7-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a08e7-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a08e7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a08e7-149">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a08e7-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="a08e7-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a08e7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a08e7-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a08e7-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a08e7-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a08e7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a08e7-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a08e7-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08e7-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a08e7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08e7-155">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="a08e7-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="a08e7-156">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="a08e7-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="a08e7-157">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="a08e7-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="a08e7-158">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="a08e7-158">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="a08e7-159">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="a08e7-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





