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
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310567"
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

*RequestType* \[ in\]
</dt> <dd>

Mappa di bit che identifica il tipo di richiesta del descrittore e il destinatario. Il tipo di richiesta può essere ' standard ',' Class ' o ' specifico del fornitore '. Il destinatario può essere ' Device ',' Interface ',' endpoint ' o ' other '. Vedere la specifica USB per i valori appropriati per ogni bit.

</dd> <dt>

*RequestValue* \[ in\]
</dt> <dd>

Contiene il tipo di descrittore nel byte elevato e l'indice del descrittore, ad esempio indice o offset nella matrice di descrittori, nel byte minimo. Per ulteriori informazioni, fare riferimento alla specifica USB.

</dd> <dt>

*RequestIndex* \[ in\]
</dt> <dd>

Definisce il codice ID lingua a 2 byte utilizzato da USBDevice quando vengono restituiti i dati del descrittore di stringa. Il parametro è in genere 0 per i descrittori non di stringa. Per ulteriori informazioni, fare riferimento alla specifica USB.

</dd> <dt>

*RequestLength* \[ in uscita\]
</dt> <dd>

In input, contiene la lunghezza (in ottetti) del descrittore che deve essere restituito. Se questo valore è inferiore alla lunghezza effettiva del descrittore, verrà restituita solo la lunghezza richiesta. Se è maggiore della lunghezza effettiva, viene restituita la lunghezza effettiva. Nell'output, questo parametro è la lunghezza, in ottetti, del buffer restituito. Se il descrittore richiesto non esiste, il contenuto di questo parametro non è definito.

</dd> <dt>

*Buffer* \[ out\]
</dt> <dd>

Restituisce le informazioni sul descrittore richieste. Se il descrittore non esiste, il contenuto del parametro non è definito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> </dl>

 

 




