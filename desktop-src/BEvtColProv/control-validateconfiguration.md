---
description: Convalidare la correttezza di un testo di configurazione senza impostarlo come attivo. Restituisce 1 in seguito all'esito positivo, 0 in seguito a un errore.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Metodo ValidateConfiguration della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965909"
---
# <a name="validateconfiguration-method-of-the-control-class"></a>Metodo ValidateConfiguration della classe Control

Convalidare la correttezza di un testo di configurazione senza impostarlo come attivo. Restituisce 1 in seguito all'esito positivo, 0 in seguito a un errore.

## <a name="syntax"></a>Sintassi


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Configurazione* \[ di in\]
</dt> <dd>

Configurazione da verificare.

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Quando questo metodo restituisce, se si è verificato un errore, questo parametro contiene una descrizione dell'errore di convalida per l'operazione.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

Quando questo metodo restituisce un risultato, questo parametro contiene una descrizione degli avvisi di convalida per l'operazione.

Stringa di testo con avvisi.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

Quando questo metodo restituisce un risultato, questo parametro contiene un set di informazioni sulla configurazione.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

Quando questo metodo restituisce, se si è verificato un errore di convalida, questo parametro indica il tipo di errore.

I valori possibili sono:

<dt>

0
</dt> <dd>

Argomento mancante.

</dd> <dt>

1
</dt> <dd>

Il formato dell'argomento non è valido.

</dd> <dt>

2
</dt> <dd>

Un argomento di configurazione non è valido.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

<dl> <dt>


</dt> <dd>

0

Errore

</dd> <dt>


</dt> <dd>

1

Operazione completata

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Radice \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




