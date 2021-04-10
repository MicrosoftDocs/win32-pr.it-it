---
title: Metodi di proprietà IADsClass (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsClass ottengono o impostano le proprietà seguenti. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsClass ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120754"
---
# <a name="iadsclass-property-methods"></a><span data-ttu-id="ebff3-105">Metodi di proprietà IADsClass</span><span class="sxs-lookup"><span data-stu-id="ebff3-105">IADsClass Property Methods</span></span>

<span data-ttu-id="ebff3-106">I metodi di proprietà dell'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) ottengono o impostano le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ebff3-106">The property methods of the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface get or set the following properties.</span></span> <span data-ttu-id="ebff3-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ebff3-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ebff3-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ebff3-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ebff3-109">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="ebff3-109">**Abstract**</span></span>
<span data-ttu-id="ebff3-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-111">Valore booleano che indica se questa classe è astratta o non astratta.</span><span class="sxs-lookup"><span data-stu-id="ebff3-111">Boolean value that indicates if this class is Abstract or non-abstract.</span></span> <span data-ttu-id="ebff3-112">Se è **true**, questa classe è una classe astratta e non è possibile crearne un'istanza direttamente nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="ebff3-112">When **TRUE**, this class is an Abstract class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="ebff3-113">Le classi astratte possono essere utilizzate solo come classi super.</span><span class="sxs-lookup"><span data-stu-id="ebff3-113">Abstract classes can only be used as super classes.</span></span>

<dt>

<span data-ttu-id="ebff3-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-115">Tipo di dati di scripting: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ebff3-115">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-116">**AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="ebff3-116">**AuxDerivedFrom**</span></span>
<span data-ttu-id="ebff3-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-118">Matrice di stringhe ADsPath che indicano le classi ausiliarie Super da cui deriva questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebff3-118">Array of ADsPath strings that indicate the super Auxiliary classes this class derives from.</span></span>

<dt>

<span data-ttu-id="ebff3-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-120">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ebff3-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-121">**Ausiliario**</span><span class="sxs-lookup"><span data-stu-id="ebff3-121">**Auxiliary**</span></span>
<span data-ttu-id="ebff3-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-123">Valore booleano che indica se questa classe è ausiliaria o meno.</span><span class="sxs-lookup"><span data-stu-id="ebff3-123">Boolean value that indicates whether or not this class is Auxiliary.</span></span> <span data-ttu-id="ebff3-124">Se è **true**, questa classe è una classe ausiliaria e non è possibile crearne un'istanza direttamente nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="ebff3-124">When **TRUE**, this class is an Auxiliary class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="ebff3-125">Le classi ausiliarie possono essere utilizzate solo come classi super di altre classi ausiliarie o come origine di proprietà aggiuntive nelle classi strutturali.</span><span class="sxs-lookup"><span data-stu-id="ebff3-125">Auxiliary classes can only be used as super classes of other Auxiliary classes or as a source of additional properties on structural classes.</span></span>

<dt>

<span data-ttu-id="ebff3-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-127">Tipo di dati di scripting: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ebff3-127">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-128">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="ebff3-128">**CLSID**</span></span>
<span data-ttu-id="ebff3-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-130">CLSID facoltativo specifico del provider che identifica l'oggetto COM che implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebff3-130">Optional provider-specific CLSID identifying the COM object that implements this class.</span></span>

<dt>

<span data-ttu-id="ebff3-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-132">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebff3-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-133">**Contenitore**</span><span class="sxs-lookup"><span data-stu-id="ebff3-133">**Container**</span></span>
<span data-ttu-id="ebff3-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-135">Valore booleano che indica se questa classe può essere un contenitore di altre classi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="ebff3-135">Boolean value that indicates if this class can be a container of other object classes.</span></span> <span data-ttu-id="ebff3-136">Se questo valore è **true**, è possibile chiamare il metodo **get \_ container** per ottenere una matrice delle classi di oggetti che questa classe può contenere.</span><span class="sxs-lookup"><span data-stu-id="ebff3-136">If this value is **TRUE**, you can call the **get\_Container** method to get an array of the object classes that this class can contain.</span></span>

<dt>

<span data-ttu-id="ebff3-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-138">Tipo di dati di scripting: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ebff3-138">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-139">**Contenimento**</span><span class="sxs-lookup"><span data-stu-id="ebff3-139">**Containment**</span></span>
<span data-ttu-id="ebff3-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-141">Matrice **BSTR** in cui ogni elemento è il nome di una classe di oggetti che questa classe può contenere.</span><span class="sxs-lookup"><span data-stu-id="ebff3-141">A **BSTR** array in which each element is the name of an object class that this class can contain.</span></span>

<dt>

<span data-ttu-id="ebff3-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-143">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ebff3-143">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-144">**Estratta da**</span><span class="sxs-lookup"><span data-stu-id="ebff3-144">**DerivedFrom**</span></span>
<span data-ttu-id="ebff3-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-146">Matrice di stringhe ADsPath che indicano da quali classi è stata derivata questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebff3-146">Array of ADsPath strings that indicate which classes this class was derived from.</span></span>

<dt>

<span data-ttu-id="ebff3-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-148">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ebff3-148">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-149">**HelpFileContext**</span><span class="sxs-lookup"><span data-stu-id="ebff3-149">**HelpFileContext**</span></span>
<span data-ttu-id="ebff3-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-151">ID del contesto in **HelpFileName** in cui è possibile trovare informazioni specifiche per questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebff3-151">Context ID inside **HelpFileName** where specific information for this class can be found.</span></span>

<dt>

<span data-ttu-id="ebff3-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-153">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ebff3-153">Scripting data type: **long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-154">**HelpFileName**</span><span class="sxs-lookup"><span data-stu-id="ebff3-154">**HelpFileName**</span></span>
<span data-ttu-id="ebff3-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-156">Nome di un file della guida che contiene ulteriori informazioni sugli oggetti di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebff3-156">Name of a help file that contains more information about objects of this class.</span></span>

<dt>

<span data-ttu-id="ebff3-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-158">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebff3-158">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-159">**MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="ebff3-159">**MandatoryProperties**</span></span>
<span data-ttu-id="ebff3-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-161">**SAFEARRAY** di **varianti** che elenca le proprietà che devono essere impostate affinché questa classe venga scritta nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="ebff3-161">**SAFEARRAY** of **VARIANT** s that lists the properties that must be set for this class to be written to storage.</span></span> <span data-ttu-id="ebff3-162">Se la classe contiene solo una proprietà, **get \_ MandatoryProperties** restituirà un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="ebff3-162">If the class only contains one property, then **get\_MandatoryProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="ebff3-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-164">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ebff3-164">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-165">**NamingProperties**</span><span class="sxs-lookup"><span data-stu-id="ebff3-165">**NamingProperties**</span></span>
<span data-ttu-id="ebff3-166"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-166"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-167">**SAFEARRAY** di **BSTR** che elenca le proprietà utilizzate per denominare gli attributi di questa classe dello schema.</span><span class="sxs-lookup"><span data-stu-id="ebff3-167">**SAFEARRAY** of **BSTR** s that lists the properties used to name attributes of this schema class.</span></span>

<dt>

<span data-ttu-id="ebff3-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-169">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ebff3-169">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-170">**OID**</span><span class="sxs-lookup"><span data-stu-id="ebff3-170">**OID**</span></span>
<span data-ttu-id="ebff3-171"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-171"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-172">Identificatore di oggetto specifico del provider che definisce questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebff3-172">Provider-specific Object Identifier that defines this class.</span></span> <span data-ttu-id="ebff3-173">Viene fornito per consentire l'estensione dello schema, utilizzando Active Directory, nei servizi directory che richiedono OID specifici del provider per le classi.</span><span class="sxs-lookup"><span data-stu-id="ebff3-173">This is provided to allow schema extension, using Active Directory, in directory services that require provider-specific OIDs for classes.</span></span>

<dt>

<span data-ttu-id="ebff3-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-175">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebff3-175">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-176">**OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="ebff3-176">**OptionalProperties**</span></span>
<span data-ttu-id="ebff3-177"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-177"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-178">**SAFEARRAY** di **varianti** che elenca le proprietà facoltative per questa classe dello schema.</span><span class="sxs-lookup"><span data-stu-id="ebff3-178">**SAFEARRAY** of **VARIANT** s that lists the optional properties for this schema class.</span></span> <span data-ttu-id="ebff3-179">Se la classe contiene solo una proprietà, **get \_ OptionalProperties** restituirà un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="ebff3-179">If the class only contains one property, then **get\_OptionalProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="ebff3-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-181">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ebff3-181">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-182">**PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="ebff3-182">**PossibleSuperiors**</span></span>
<span data-ttu-id="ebff3-183"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-183"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-184">Matrice di stringhe ADsPath che indicano le classi dello schema che possono contenere istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebff3-184">Array of ADsPath strings that indicate the schema classes that can contain instances of this class.</span></span>

<dt>

<span data-ttu-id="ebff3-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ebff3-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-186">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ebff3-186">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebff3-187">**PrimaryInterface**</span><span class="sxs-lookup"><span data-stu-id="ebff3-187">**PrimaryInterface**</span></span>
<span data-ttu-id="ebff3-188"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ebff3-188"></dt> <dd> <dl></span></span>

<span data-ttu-id="ebff3-189">GUID dell'identificatore specifico del provider facoltativo che associa un'interfaccia a oggetti di questa classe dello schema.</span><span class="sxs-lookup"><span data-stu-id="ebff3-189">Optional provider-specific identifier GUID that associates an interface to objects of this schema class.</span></span> <span data-ttu-id="ebff3-190">Ad esempio, la classe "User" che supporta [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) e **PrimaryInterface** è identificata da **IID \_ IADsUser**.</span><span class="sxs-lookup"><span data-stu-id="ebff3-190">For example, the "User" class that supports [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) and **PrimaryInterface** is identified by **IID\_IADsUser**.</span></span> <span data-ttu-id="ebff3-191">Deve essere nel formato stringa standard di un GUID, come definito da COM.</span><span class="sxs-lookup"><span data-stu-id="ebff3-191">This must be in the standard string format of a GUID, as defined by COM.</span></span> <span data-ttu-id="ebff3-192">Questo GUID è il valore che viene visualizzato nella proprietà [**IADs:: Get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) nelle istanze di questa classe per i provider che implementano questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ebff3-192">This GUID is the value that appears in the [**IADs::get\_GUID**](/windows/desktop/api/Iads/nn-iads-iads) property in instances of this class for providers that implement this property.</span></span> <span data-ttu-id="ebff3-193">L'identificazione di una classe di schema per IID dell'interfaccia principale del codice della classe consente l'utilizzo di **QueryInterface** in fase di esecuzione per determinare se un oggetto è della classe desiderata.</span><span class="sxs-lookup"><span data-stu-id="ebff3-193">Identifying a schema class by IID of the class code's primary interface enables the use of **QueryInterface** at run time to determine whether an object is of the desired class.</span></span>

<dt>

<span data-ttu-id="ebff3-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ebff3-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebff3-195">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebff3-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="ebff3-196">Esempio</span><span class="sxs-lookup"><span data-stu-id="ebff3-196">Examples</span></span>

<span data-ttu-id="ebff3-197">Nell'esempio di codice seguente viene illustrato come utilizzare l'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) per determinare se un oggetto può essere un contenitore e, in caso affermativo, elenca i nomi di tutti gli oggetti contenuti.</span><span class="sxs-lookup"><span data-stu-id="ebff3-197">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



<span data-ttu-id="ebff3-198">Nell'esempio di codice seguente viene illustrato come utilizzare l'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) per determinare se un oggetto può essere un contenitore e, in caso affermativo, elenca i nomi di tutti gli oggetti contenuti.</span><span class="sxs-lookup"><span data-stu-id="ebff3-198">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="ebff3-199">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebff3-199">Requirements</span></span>



| <span data-ttu-id="ebff3-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebff3-200">Requirement</span></span> | <span data-ttu-id="ebff3-201">Valore</span><span class="sxs-lookup"><span data-stu-id="ebff3-201">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebff3-202">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebff3-202">Minimum supported client</span></span><br/> | <span data-ttu-id="ebff3-203">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebff3-203">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ebff3-204">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebff3-204">Minimum supported server</span></span><br/> | <span data-ttu-id="ebff3-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebff3-205">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ebff3-206">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebff3-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebff3-207"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebff3-207"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ebff3-208">DLL</span><span class="sxs-lookup"><span data-stu-id="ebff3-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebff3-209"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebff3-209"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebff3-210">IID</span><span class="sxs-lookup"><span data-stu-id="ebff3-210">IID</span></span><br/>                      | <span data-ttu-id="ebff3-211">IID \_ IADsClass è definito come C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="ebff3-211">IID\_IADsClass is defined as C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ebff3-212">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebff3-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebff3-213">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="ebff3-213">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="ebff3-214">**IADsClass:: Qualifiers**</span><span class="sxs-lookup"><span data-stu-id="ebff3-214">**IADsClass::Qualifiers**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





