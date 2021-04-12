---
description: Recupera il valore di un'opzione di accesso Microsoft .NET Passport specifica.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'Metodo IPassportManager3:: get_Option'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401364"
---
# <a name="ipassportmanager3get_option-method"></a>Metodo dell'opzione IPassportManager3:: Get \_

Recupera il valore di un'opzione di accesso Microsoft .NET Passport specifica.

> [!Note]  
> Il metodo dell' **\_ opzione Get** appartiene all'interfaccia [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Questo argomento integra la documentazione iniziale.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* \[ in\]
</dt> <dd>

Opzione di accesso da recuperare. Attualmente, l'unica opzione supportata è "iMode".

</dd> <dt>

*pval* \[ out\]
</dt> <dd>

Puntatore a un oggetto **Variant** (VT \_ bool) che riceve il valore dell'opzione. Questo valore può essere true o false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK quando il metodo ha esito positivo.

## <a name="remarks"></a>Commenti

Questo metodo viene fornito con le versioni precedenti di Passport SDK.

 

 
