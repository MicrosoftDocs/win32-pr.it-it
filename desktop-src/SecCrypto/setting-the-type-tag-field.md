---
description: Le variabili di tipo VARIANT hanno un campo di tag del tipo VT che indica il tipo di dati dei dati.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Impostazione del campo tag del tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225865"
---
# <a name="setting-the-type-tag-field"></a><span data-ttu-id="ab8e1-103">Impostazione del campo tag del tipo</span><span class="sxs-lookup"><span data-stu-id="ab8e1-103">Setting the Type Tag Field</span></span>

<span data-ttu-id="ab8e1-104">Le variabili di tipo **Variant** hanno un campo di tag del tipo **VT** che indica il tipo di dati dei dati.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-104">**VARIANT** type variables have a type tag field **vt** that indicates the data type of the data.</span></span> <span data-ttu-id="ab8e1-105">I valori restituiti del tipo **Variant** vengono restituiti dai metodi con il campo del tag type impostato sul tipo di dati del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-105">**VARIANT** type return values are returned by methods with the type tag field set to the data type of the return value.</span></span> <span data-ttu-id="ab8e1-106">I parametri di input di tipo **Variant** in una chiamata al metodo devono avere il campo dei tag type impostato dall'applicazione su uno dei valori supportati.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-106">**VARIANT** type input parameters in a method call must have the type tag field set by the application to one of the supported values.</span></span> <span data-ttu-id="ab8e1-107">Di seguito è riportata la corrispondenza dei tipi di parametro con i tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-107">The correspondence of parameter types to data types is as follows.</span></span>



| <span data-ttu-id="ab8e1-108">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="ab8e1-108">Parameter type</span></span>              | <span data-ttu-id="ab8e1-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ab8e1-109">Data type</span></span>                                      |
|-----------------------------|------------------------------------------------|
| <span data-ttu-id="ab8e1-110">PROPTYPE \_ Long</span><span class="sxs-lookup"><span data-stu-id="ab8e1-110">PROPTYPE\_LONG</span></span><br/>   | <span data-ttu-id="ab8e1-111">VT \_ I2 o VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ab8e1-111">VT\_I2 or VT\_I4</span></span><br/>                    |
| <span data-ttu-id="ab8e1-112">\_Data PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="ab8e1-112">PROPTYPE\_DATE</span></span><br/>   | <span data-ttu-id="ab8e1-113">\_Data VT</span><span class="sxs-lookup"><span data-stu-id="ab8e1-113">VT\_DATE</span></span><br/>                            |
| <span data-ttu-id="ab8e1-114">\_binario PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="ab8e1-114">PROPTYPE\_BINARY</span></span><br/> | <span data-ttu-id="ab8e1-115">VT \_ BSTR o (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="ab8e1-115">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |
| <span data-ttu-id="ab8e1-116">\_stringa PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="ab8e1-116">PROPTYPE\_STRING</span></span><br/> | <span data-ttu-id="ab8e1-117">VT \_ BSTR o (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="ab8e1-117">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |



 

<span data-ttu-id="ab8e1-118">Nell'esempio seguente viene illustrato come inizializzare i tipi di dati Variant elencati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-118">The following example shows how to initialize the variant data types listed above.</span></span>


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




