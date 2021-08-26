---
description: Recupera informazioni sul set di moduli attualmente caricato per il sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Funzione AuxKlibQueryModuleInformation (Aux \_ klib.h)
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
ms.openlocfilehash: be734583c8b7d02be4c498bc75069a0c813565d48aea3db3826712d6375e72b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045316"
---
# <a name="auxklibquerymoduleinformation-function"></a>Funzione AuxKlibQueryModuleInformation

Recupera informazioni sul set di moduli attualmente caricato per il sistema.

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

*BufferSize* \[ in, out\]
</dt> <dd>

In input, le dimensioni del buffer *QueryInfo,* in byte. Nell'output riceve le dimensioni effettive richieste. Poiché l'elenco dei moduli di sistema può cambiare tra le chiamate, questo valore può cambiare anche tra le chiamate.

</dd> <dt>

*ElementSize* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, di un elemento della matrice. Queste dimensioni determinano il formato dell'output.

</dd> <dt>

*QueryInfo* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve le informazioni sul modulo. Queste informazioni vengono restituite in una matrice i cui elementi sono una delle strutture seguenti: [**AUX \_ MODULE BASIC \_ \_ INFO**](aux-module-basic-info-struct.md) o [**AUX MODULE EXTENDED \_ \_ \_ INFO**](aux-module-extended-info-struct.md). La struttura specifica usata dipende dalle dimensioni dell'elemento specificate.

Se questo parametro è **NULL,** la funzione restituisce le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di stato definiti in Ntstatus.h, disponibile in WDK.

## <a name="remarks"></a>Commenti

È necessario chiamare la [**funzione AuxKlibInitialize**](auxklibinitialize-func.md) prima di chiamare questa funzione.

La libreria di oggetti che implementa questa API può essere scaricata da [qui.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|------------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria API ausiliaria versione 1.0 o successiva<br/>                            |
| Intestazione<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl>   |
| Libreria<br/>         | <dl> <dt>Aux \_ klib.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**INFORMAZIONI DI \_ BASE SUL \_ MODULO AUX \_**](aux-module-basic-info-struct.md)
</dt> <dt>

[**INFORMAZIONI ESTESE \_ DEL \_ MODULO AUX \_**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




