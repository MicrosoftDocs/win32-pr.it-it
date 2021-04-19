---
description: Sottoclassi automaticamente e aggiunge effetti 3D a tutte le finestre di dialogo nell'applicazione.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331971"
---
# <a name="ctl3dautosubclass-function"></a>Ctl3dAutoSubclass (funzione)

Sottoclassi automaticamente e aggiunge effetti 3D a tutte le finestre di dialogo nell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hinstApp* 
</dt> <dd>

Handle per l'applicazione da registrare come client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** a meno che non esista una delle condizioni seguenti, nel qual caso restituisce **false**:

-   CTL3D è in esecuzione in Windows versione 3,0 o versioni precedenti.
-   In CTL3D non è disponibile spazio nelle tabelle per l'applicazione corrente. CTL3D è in grado di servire fino a 32 applicazioni nello stesso momento.
-   CTL3D non è in grado di installare il relativo hook CBT.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
