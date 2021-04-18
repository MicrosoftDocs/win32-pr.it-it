---
description: Recupera le informazioni sul set di moduli attualmente caricato per il sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Funzione AuxKlibQueryModuleInformation (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325406"
---
# <a name="auxklibquerymoduleinformation-function"></a>AuxKlibQueryModuleInformation (funzione)

Recupera le informazioni sul set di moduli attualmente caricato per il sistema.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BufferSize* \[ in uscita\]
</dt> <dd>

In input, dimensione del buffer *QueryInfo* in byte. Nell'output, riceve le dimensioni effettive richieste. Poiché l'elenco dei moduli di sistema può variare tra le chiamate, questo valore può anche variare tra le chiamate.

</dd> <dt>

*ElementSize* \[ in\]
</dt> <dd>

Dimensione, in byte, di un elemento di matrice. Questa dimensione determina il formato dell'output.

</dd> <dt>

*QueryInfo* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve le informazioni sul modulo. Queste informazioni vengono restituite in una matrice i cui elementi sono una delle seguenti strutture: [**aux \_ module \_ Basic \_ info**](aux-module-basic-info-struct.md) o [**aux \_ module \_ Extended \_ info**](aux-module-extended-info-struct.md). La struttura specifica utilizzata dipende dalla dimensione dell'elemento specificata.

Se questo parametro è **null**, la funzione restituisce la dimensione del buffer richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di stato definiti in ntstatus. h, disponibile in WDK.

## <a name="remarks"></a>Commenti

Prima di chiamare questa funzione, è necessario chiamare la funzione [**AuxKlibInitialize**](auxklibinitialize-func.md) .

La libreria di oggetti che implementa questa API può essere scaricata da [qui](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|------------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Libreria API ausiliaria Windows versione 1,0 o successiva<br/>                            |
| Intestazione<br/>          | <dl> <dt>Aux \_ klib. h</dt> </dl>   |
| Libreria<br/>         | <dl> <dt>Aux \_ klib. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**\_informazioni di \_ base sul modulo aux \_**](aux-module-basic-info-struct.md)
</dt> <dt>

[**\_ \_ informazioni estese sul modulo aux \_**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




