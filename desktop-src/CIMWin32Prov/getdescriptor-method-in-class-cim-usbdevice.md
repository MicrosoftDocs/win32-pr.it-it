---
description: Il metodo GetDescriptor restituisce il descrittore del dispositivo USB come specificato dai parametri di input.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Metodo GetDescriptor della CIM_USBDevice classe (Wmcodecdsp.h)
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
- CIMWin32.dll
ms.openlocfilehash: 1288ab1c00ec51c61d3a5e2f7c013ca1e3728fc88087092868421f8e11b7f0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077541"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a>Metodo GetDescriptor della CIM_USBDevice classe (Wmcodecdsp.h)

Il **metodo GetDescriptor** restituisce il descrittore del dispositivo USB come specificato dai parametri di input.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

Identificatore mappato a bit per il tipo di richiesta del descrittore e il destinatario. Fare riferimento alla specifica USB per i valori appropriati per ogni bit.

</dd> <dt>

*RequestValue* \[ Pollici\]
</dt> <dd>

Contiene il tipo di descrittore nel byte alto e l'indice del descrittore (ad esempio, indice o offset nella matrice del descrittore) nel byte basso. Per altre informazioni, vedere la specifica USB.

</dd> <dt>

*RequestIndex* \[ Pollici\]
</dt> <dd>

Specifica il codice dell'identificatore di lingua a 2 byte usato dal dispositivo USB quando vengono restituiti i dati del descrittore di stringa. Il parametro è in genere 0 (zero) per i descrittori non stringa. Per altre informazioni, vedere la specifica USB.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

In input, lunghezza (in ottetti) del descrittore che deve essere restituito. Se questo valore è minore della lunghezza effettiva del descrittore, viene restituita solo la lunghezza richiesta. Se è maggiore della lunghezza effettiva, viene restituita la lunghezza effettiva.

Nell'output, la lunghezza (in ottetti) del buffer restituito. Se il descrittore richiesto non esiste, il contenuto di questo parametro non è definito.

</dd> <dt>

*Buffer* \[ Cambio\]
</dt> <dd>

Restituisce le informazioni sul descrittore richiesto. Se il descrittore non esiste, il contenuto di questo parametro non è definito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il descrittore USB viene restituito correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore. In una sottoclasse il set di possibili codici restituiti può essere specificato usando un **qualificatore ValueMap** nel metodo . Le stringhe in cui viene convertito il contenuto del mofqualifier possono essere specificate anche nella sottoclasse come qualificatore di matrice **Values.**

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ USBDevice**](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> </dl>

 

