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
# <a name="inondelegatingunknown"></a>INonDelegatingUnknown

L' `INonDelegatingUnknown` interfaccia è una versione di **IUnknown** che viene rinominata per abilitare il supporto per le interfacce **IUnknown** non delegate e Delegate nello stesso oggetto com.

## <a name="syntax"></a>Sintassi


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Osservazioni

Per usare `INonDelegatingUnknown` per l'ereditarietà multipla, seguire questa procedura.

1.  Derivare la classe da un'interfaccia, ad esempio IMyInterface.
2.  Includere [**Declare \_ IUnknown**](declare-iunknown.md) nella definizione della classe per dichiarare le implementazioni di **QueryInterface**, **AddRef** e **Release** che chiamano l'oggetto sconosciuto esterno.
3.  Eseguire l'override di **NonDelegatingQueryInterface** per esporre IMyInterface con codice simile al seguente:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Dichiarare e implementare le funzioni membro di IMyInterface.

Per usare `INonDelegatingUnknown` per le interfacce nidificate, seguire questa procedura:

1.  Dichiarare una classe derivata da [**CUnknown**](cunknown.md).
2.  Includere [**Declare \_ IUnknown**](declare-iunknown.md) nella definizione della classe.
3.  Eseguire l'override di **NonDelegatingQueryInterface** per esporre IMyInterface con il codice seguente:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implementare le funzioni membro di IMyInterface. Usare [**CUnknown:: GetOwner**](cunknown-getowner.md) per accedere alla classe di oggetti com.
5.  Nella classe di oggetti COM, rendere la classe annidata un elemento Friend della classe di oggetti COM e dichiarare un'istanza della classe annidata come membro della classe di oggetti COM.

Poiché è necessario passare sempre l'oggetto sconosciuto esterno e un **HRESULT** al costruttore [**CUnknown**](cunknown.md) , non è possibile usare un costruttore predefinito. È necessario rendere la variabile membro un puntatore alla classe ed effettuare una nuova chiamata nel costruttore per crearla effettivamente.

Eseguire l'override di **NonDelegatingQueryInterface** con codice simile al seguente:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



È possibile disporre di classi miste che supportano alcune interfacce tramite ereditarietà multipla e alcune interfacce tramite classi annidate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni helper COM**](com-helper-functions.md)
</dt> </dl>

 

 




