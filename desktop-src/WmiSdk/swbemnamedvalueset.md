---
description: Un oggetto SWbemNamedValueSet è una raccolta di oggetti SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Oggetto SWbemNamedValueSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309831"
---
# <a name="swbemnamedvalueset-object"></a><span data-ttu-id="2ad33-103">Oggetto SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="2ad33-103">SWbemNamedValueSet object</span></span>

<span data-ttu-id="2ad33-104">Un oggetto **SWbemNamedValueSet** è una raccolta di oggetti [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="2ad33-104">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) objects.</span></span> <span data-ttu-id="2ad33-105">I metodi e le proprietà di **SWbemNamedValueSet** vengono utilizzati principalmente per inviare più informazioni ai provider quando si inviano determinate chiamate a WMI.</span><span class="sxs-lookup"><span data-stu-id="2ad33-105">The methods and properties of **SWbemNamedValueSet** are used principally to send more information to providers when submitting certain calls to WMI.</span></span> <span data-ttu-id="2ad33-106">Tutte le chiamate in [**SWbemServices**](swbemservices.md)e alcune chiamate in [**SWbemObject**](swbemobject.md)accettano un parametro facoltativo che è un oggetto di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="2ad33-106">All calls in [**SWbemServices**](swbemservices.md), and some calls in [**SWbemObject**](swbemobject.md), take an optional parameter that is an object of this type.</span></span> <span data-ttu-id="2ad33-107">Un client può aggiungere informazioni a un oggetto **SWbemNamedValueSet** e inviare l'oggetto **SWbemNamedValueSet** alla chiamata come uno dei parametri.</span><span class="sxs-lookup"><span data-stu-id="2ad33-107">A client can add information to an **SWbemNamedValueSet** object, and send the **SWbemNamedValueSet** object with the call as one of the parameters.</span></span> <span data-ttu-id="2ad33-108">Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="2ad33-108">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="2ad33-109">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="2ad33-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

> [!Note]  
> <span data-ttu-id="2ad33-110">Importante: se possibile, non utilizzare questo meccanismo perché può interrompere il modello di accesso uniforme che è la base di WMI.</span><span class="sxs-lookup"><span data-stu-id="2ad33-110">Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI.</span></span> <span data-ttu-id="2ad33-111">Se un provider utilizza questo meccanismo, è importante che questo meccanismo venga utilizzato nel modo più sporadico possibile.</span><span class="sxs-lookup"><span data-stu-id="2ad33-111">If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible.</span></span> <span data-ttu-id="2ad33-112">Se un provider richiede una grande quantità di informazioni di contesto molto specifiche per rispondere a una richiesta, tutti i client devono essere codificati per fornire queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="2ad33-112">If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information.</span></span> <span data-ttu-id="2ad33-113">Questo meccanismo consente di accedere a tali provider, se necessario.</span><span class="sxs-lookup"><span data-stu-id="2ad33-113">This mechanism allows you to access such providers, if necessary.</span></span>

 

<span data-ttu-id="2ad33-114">Un oggetto **SWbemNamedValueSet** è una raccolta di elementi [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="2ad33-114">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) elements.</span></span> <span data-ttu-id="2ad33-115">Questi elementi vengono aggiunti alla raccolta usando il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="2ad33-115">These items are added to the collection using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span> <span data-ttu-id="2ad33-116">Vengono rimossi usando il metodo [**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md) e recuperati usando il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="2ad33-116">They are removed using the [**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) method and retrieved using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="2ad33-117">È possibile accedere ai metodi per inserire le informazioni di contesto richieste da un provider dinamico.</span><span class="sxs-lookup"><span data-stu-id="2ad33-117">You can access the methods to fill in any context information that is required by a dynamic provider.</span></span> <span data-ttu-id="2ad33-118">Dopo aver chiamato uno dei metodi [**SWbemServices**](swbemservices.md) , è possibile riutilizzare l'oggetto **SWbemNamedValueSet** per un'altra chiamata.</span><span class="sxs-lookup"><span data-stu-id="2ad33-118">After you call one of the [**SWbemServices**](swbemservices.md) methods, you can reuse the **SWbemNamedValueSet** object for another call.</span></span>

<span data-ttu-id="2ad33-119">Il provider sottostante determina le informazioni contenute in un oggetto **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="2ad33-119">The underlying provider determines the information that is contained in an **SWbemNamedValueSet** object.</span></span> <span data-ttu-id="2ad33-120">WMI non utilizza le informazioni, ma semplicemente lo trasmette al provider.</span><span class="sxs-lookup"><span data-stu-id="2ad33-120">WMI makes no use of the information, but simply forwards it to the provider.</span></span> <span data-ttu-id="2ad33-121">I provider devono pubblicare le informazioni sul contesto necessarie per soddisfare le richieste.</span><span class="sxs-lookup"><span data-stu-id="2ad33-121">Providers must publish the context information they require to service requests.</span></span>

## <a name="members"></a><span data-ttu-id="2ad33-122">Membri</span><span class="sxs-lookup"><span data-stu-id="2ad33-122">Members</span></span>

<span data-ttu-id="2ad33-123">L'oggetto **SWbemNamedValueSet** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2ad33-123">The **SWbemNamedValueSet** object has these types of members:</span></span>

-   [<span data-ttu-id="2ad33-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="2ad33-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ad33-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ad33-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ad33-126">Metodi</span><span class="sxs-lookup"><span data-stu-id="2ad33-126">Methods</span></span>

<span data-ttu-id="2ad33-127">L'oggetto **SWbemNamedValueSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2ad33-127">The **SWbemNamedValueSet** object has these methods.</span></span>



| <span data-ttu-id="2ad33-128">Metodo</span><span class="sxs-lookup"><span data-stu-id="2ad33-128">Method</span></span>                                            | <span data-ttu-id="2ad33-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ad33-129">Description</span></span>                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ad33-130">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="2ad33-130">**Add**</span></span>](swbemnamedvalueset-add.md)             | <span data-ttu-id="2ad33-131">Aggiunge un oggetto [**SWbemNamedValue**](swbemnamedvalue.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="2ad33-131">Adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span><br/>                                                  |
| [<span data-ttu-id="2ad33-132">**Clone**</span><span class="sxs-lookup"><span data-stu-id="2ad33-132">**Clone**</span></span>](swbemnamedvalueset-clone.md)         | <span data-ttu-id="2ad33-133">Crea una copia di questa raccolta **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="2ad33-133">Makes a copy of this **SWbemNamedValueSet** collection.</span></span><br/>                                                                       |
| [<span data-ttu-id="2ad33-134">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="2ad33-134">**DeleteAll**</span></span>](swbemnamedvalueset-deleteall.md) | <span data-ttu-id="2ad33-135">Rimuove tutti gli elementi dalla raccolta, rendendo vuoto l'oggetto **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="2ad33-135">Removes all items from the collection, making the **SWbemNamedValueSet** object empty.</span></span><br/>                                        |
| [<span data-ttu-id="2ad33-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2ad33-136">**Item**</span></span>](swbemnamedvalueset-item.md)           | <span data-ttu-id="2ad33-137">Recupera un oggetto [**SWbemNamedValue**](swbemnamedvalue.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="2ad33-137">Retrieves an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span> <span data-ttu-id="2ad33-138">Si tratta del metodo predefinito dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2ad33-138">This is the default method of the object.</span></span><br/> |
| [<span data-ttu-id="2ad33-139">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="2ad33-139">**Remove**</span></span>](swbemnamedvalueset-remove.md)       | <span data-ttu-id="2ad33-140">Rimuove un oggetto [**SWbemNamedValue**](swbemnamedvalue.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="2ad33-140">Removes an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span><br/>                                             |



 

### <a name="properties"></a><span data-ttu-id="2ad33-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ad33-141">Properties</span></span>

<span data-ttu-id="2ad33-142">L'oggetto **SWbemNamedValueSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2ad33-142">The **SWbemNamedValueSet** object has these properties.</span></span>



| <span data-ttu-id="2ad33-143">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ad33-143">Property</span></span>                                             | <span data-ttu-id="2ad33-144">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2ad33-144">Access type</span></span>          | <span data-ttu-id="2ad33-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ad33-145">Description</span></span>                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="2ad33-146">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="2ad33-146">**Count**</span></span>](swbemnamedvalueset-count.md)<br/> | <span data-ttu-id="2ad33-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2ad33-147">Read-only</span></span><br/> | <span data-ttu-id="2ad33-148">Numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="2ad33-148">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="2ad33-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="2ad33-149">Examples</span></span>

<span data-ttu-id="2ad33-150">Nell'esempio VBScript riportato di seguito viene illustrata la manipolazione dei set di valori denominati, nel caso in cui il valore denominato sia un tipo di matrice.</span><span class="sxs-lookup"><span data-stu-id="2ad33-150">The following VBScript sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="2ad33-151">Nell'esempio Perl seguente viene illustrata la manipolazione dei set di valori denominati, nel caso in cui il valore denominato sia un tipo di matrice.</span><span class="sxs-lookup"><span data-stu-id="2ad33-151">The following Perl sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="2ad33-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ad33-152">Requirements</span></span>



| <span data-ttu-id="2ad33-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ad33-153">Requirement</span></span> | <span data-ttu-id="2ad33-154">Valore</span><span class="sxs-lookup"><span data-stu-id="2ad33-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad33-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ad33-155">Minimum supported client</span></span><br/> | <span data-ttu-id="2ad33-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ad33-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ad33-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ad33-157">Minimum supported server</span></span><br/> | <span data-ttu-id="2ad33-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ad33-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ad33-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ad33-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ad33-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ad33-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ad33-161">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2ad33-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ad33-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ad33-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2ad33-163">DLL</span><span class="sxs-lookup"><span data-stu-id="2ad33-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ad33-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ad33-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2ad33-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="2ad33-165">CLSID</span></span><br/>                    | <span data-ttu-id="2ad33-166">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="2ad33-166">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="2ad33-167">IID</span><span class="sxs-lookup"><span data-stu-id="2ad33-167">IID</span></span><br/>                      | <span data-ttu-id="2ad33-168">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="2ad33-168">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="2ad33-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ad33-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad33-170">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="2ad33-170">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




