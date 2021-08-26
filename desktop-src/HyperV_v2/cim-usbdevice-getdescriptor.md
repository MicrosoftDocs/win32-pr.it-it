---
description: Restituisce il descrittore USBDevice come specificato dai parametri di input.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Metodo GetDescriptor della classe CIM_USBDevice (gestione di Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0523cc88205792f9429eb1a214d8b74a1ca4c2f2bf35813c25614f9f3c06199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980781"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>Metodo GetDescriptor della classe CIM_USBDevice (gestione di Hyper-V)

Restituisce il descrittore USBDevice come specificato dai parametri di input.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestType* \[ Pollici\]
</dt> <dd>

Mappa di bit che identifica il tipo di richiesta del descrittore e il destinatario. Il tipo di richiesta può essere 'standard', 'class' o 'vendor-specific'. Il destinatario può essere 'device', 'interface', 'endpoint' o 'other'. Fare riferimento alla specifica USB per i valori appropriati per ogni bit.

</dd> <dt>

*RequestValue* \[ Pollici\]
</dt> <dd>

Contiene il tipo di descrittore nel byte alto e l'indice del descrittore (ad esempio, indice o offset nella matrice Descriptor) nel byte basso. Per altre informazioni, vedere specifica USB.

</dd> <dt>

*RequestIndex* \[ Pollici\]
</dt> <dd>

Definisce il codice ID lingua a 2 byte usato da USBDevice durante la restituzione dei dati del descrittore di stringa. Il parametro è in genere 0 per i descrittori non stringa. Per altre informazioni, vedere specifica USB.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

In input contiene la lunghezza (in ottetti) del descrittore che deve essere restituito. Se questo valore è minore della lunghezza effettiva del descrittore, verrà restituita solo la lunghezza richiesta. Se è maggiore della lunghezza effettiva, viene restituita la lunghezza effettiva. Nell'output, questo parametro è la lunghezza, in ottetti, del buffer restituito. Se il descrittore richiesto non esiste, il contenuto di questo parametro non è definito.

</dd> <dt>

*Buffer* \[ Cambio\]
</dt> <dd>

Restituisce le informazioni sul descrittore richieste. Se il descrittore non esiste, il contenuto del parametro non è definito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> </dl>

 

 




