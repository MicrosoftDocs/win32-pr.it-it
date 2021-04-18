---
description: L'interfaccia INonDelegatingUnknown è una versione di IUnknown che viene rinominata per abilitare il supporto per le interfacce IUnknown non delegate e Delegate nello stesso oggetto COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331786"
---
# <a name="inondelegatingunknown"></a><span data-ttu-id="c46a0-103">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="c46a0-103">INonDelegatingUnknown</span></span>

<span data-ttu-id="c46a0-104">L' `INonDelegatingUnknown` interfaccia è una versione di **IUnknown** che viene rinominata per abilitare il supporto per le interfacce **IUnknown** non delegate e Delegate nello stesso oggetto com.</span><span class="sxs-lookup"><span data-stu-id="c46a0-104">The `INonDelegatingUnknown` interface is a version of **IUnknown** that is renamed to enable support for both nondelegating and delegating **IUnknown** interfaces in the same COM object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c46a0-105">Syntax</span></span>


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a><span data-ttu-id="c46a0-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c46a0-106">Remarks</span></span>

<span data-ttu-id="c46a0-107">Per usare `INonDelegatingUnknown` per l'ereditarietà multipla, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="c46a0-107">To use `INonDelegatingUnknown` for multiple inheritance, perform the following steps.</span></span>

1.  <span data-ttu-id="c46a0-108">Derivare la classe da un'interfaccia, ad esempio IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="c46a0-108">Derive your class from an interface, for example, IMyInterface.</span></span>
2.  <span data-ttu-id="c46a0-109">Includere [**Declare \_ IUnknown**](declare-iunknown.md) nella definizione della classe per dichiarare le implementazioni di **QueryInterface**, **AddRef** e **Release** che chiamano l'oggetto sconosciuto esterno.</span><span class="sxs-lookup"><span data-stu-id="c46a0-109">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition to declare implementations of **QueryInterface**, **AddRef**, and **Release** that call the outer unknown.</span></span>
3.  <span data-ttu-id="c46a0-110">Eseguire l'override di **NonDelegatingQueryInterface** per esporre IMyInterface con codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="c46a0-110">Override **NonDelegatingQueryInterface** to expose IMyInterface with code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="c46a0-111">Dichiarare e implementare le funzioni membro di IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="c46a0-111">Declare and implement the member functions of IMyInterface.</span></span>

<span data-ttu-id="c46a0-112">Per usare `INonDelegatingUnknown` per le interfacce nidificate, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="c46a0-112">To use `INonDelegatingUnknown` for nested interfaces, perform the following steps:</span></span>

1.  <span data-ttu-id="c46a0-113">Dichiarare una classe derivata da [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c46a0-113">Declare a class derived from [**CUnknown**](cunknown.md).</span></span>
2.  <span data-ttu-id="c46a0-114">Includere [**Declare \_ IUnknown**](declare-iunknown.md) nella definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="c46a0-114">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition.</span></span>
3.  <span data-ttu-id="c46a0-115">Eseguire l'override di **NonDelegatingQueryInterface** per esporre IMyInterface con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="c46a0-115">Override **NonDelegatingQueryInterface** to expose IMyInterface with the code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="c46a0-116">Implementare le funzioni membro di IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="c46a0-116">Implement the member functions of IMyInterface.</span></span> <span data-ttu-id="c46a0-117">Usare [**CUnknown:: GetOwner**](cunknown-getowner.md) per accedere alla classe di oggetti com.</span><span class="sxs-lookup"><span data-stu-id="c46a0-117">Use [**CUnknown::GetOwner**](cunknown-getowner.md) to access the COM object class.</span></span>
5.  <span data-ttu-id="c46a0-118">Nella classe di oggetti COM, rendere la classe annidata un elemento Friend della classe di oggetti COM e dichiarare un'istanza della classe annidata come membro della classe di oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="c46a0-118">In your COM object class, make the nested class a friend of the COM object class, and declare an instance of the nested class as a member of the COM object class.</span></span>

<span data-ttu-id="c46a0-119">Poiché è necessario passare sempre l'oggetto sconosciuto esterno e un **HRESULT** al costruttore [**CUnknown**](cunknown.md) , non è possibile usare un costruttore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c46a0-119">Because you must always pass the outer unknown and an **HRESULT** to the [**CUnknown**](cunknown.md) constructor, you can't use a default constructor.</span></span> <span data-ttu-id="c46a0-120">È necessario rendere la variabile membro un puntatore alla classe ed effettuare una nuova chiamata nel costruttore per crearla effettivamente.</span><span class="sxs-lookup"><span data-stu-id="c46a0-120">You have to make the member variable a pointer to the class and make a new call in your constructor to actually create it.</span></span>

<span data-ttu-id="c46a0-121">Eseguire l'override di **NonDelegatingQueryInterface** con codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="c46a0-121">Override the **NonDelegatingQueryInterface** with code such as the following:</span></span>


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



<span data-ttu-id="c46a0-122">È possibile disporre di classi miste che supportano alcune interfacce tramite ereditarietà multipla e alcune interfacce tramite classi annidate.</span><span class="sxs-lookup"><span data-stu-id="c46a0-122">You can have mixed classes that support some interfaces through multiple inheritance and some interfaces through nested classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c46a0-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c46a0-123">Requirements</span></span>



| <span data-ttu-id="c46a0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c46a0-124">Requirement</span></span> | <span data-ttu-id="c46a0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c46a0-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c46a0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c46a0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c46a0-127"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c46a0-127"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c46a0-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="c46a0-128">Library</span></span><br/> | <dl> <span data-ttu-id="c46a0-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c46a0-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c46a0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c46a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46a0-131">**Funzioni helper COM**</span><span class="sxs-lookup"><span data-stu-id="c46a0-131">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




