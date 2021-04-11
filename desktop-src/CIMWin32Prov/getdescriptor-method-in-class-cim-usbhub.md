---
description: Il metodo descrittore restituisce il descrittore dell'hub USB come specificato dai parametri di input.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Metodo GetDescriptor della classe CIM_USBHub (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966062"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a>Metodo GetDescriptor della classe CIM \_ USBHub

Il metodo **descrittore** restituisce il descrittore dell'hub USB come specificato dai parametri di input.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

Identificatore con mapping bit per il tipo di richiesta del descrittore e il destinatario. Per i valori appropriati per ogni bit, vedere la specifica USB.

</dd> <dt>

*RequestValue* \[ in\]
</dt> <dd>

Contiene il tipo di descrittore nel byte elevato e l'indice del descrittore, ad esempio indice o offset nella matrice di descrittori, nel byte minimo. Per ulteriori informazioni, vedere la specifica USB.

</dd> <dt>

*RequestIndex* \[ in\]
</dt> <dd>

Specifica il codice dell'identificatore di lingua a 2 byte usato dal dispositivo USB per la restituzione di dati del descrittore di stringa. Il parametro è in genere 0 (zero) per i descrittori non di stringa. Per ulteriori informazioni, vedere la specifica USB.

</dd> <dt>

*RequestLength* \[ in uscita\]
</dt> <dd>

In input, lunghezza (in ottetti) del descrittore che deve essere restituito. Se questo valore è inferiore alla lunghezza effettiva del descrittore, viene restituita solo la lunghezza richiesta. Se è maggiore della lunghezza effettiva, viene restituita la lunghezza effettiva.

Nell'output, la lunghezza (in ottetti) del buffer restituito. Se il descrittore richiesto non esiste, il contenuto di questo parametro non è definito.

</dd> <dt>

*Buffer* \[ out\]
</dt> <dd>

Il buffer restituisce le informazioni del descrittore richieste. Se il descrittore non esiste, il contenuto del buffer non è definito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se il descrittore USB viene restituito correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore. In una sottoclasse, il set di possibili codici restituiti può essere specificato utilizzando un qualificatore **ValueMap** nel metodo. Le stringhe a cui viene convertito il contenuto **mofqualifier** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Usbhub CIM**](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[**\_Usbhub CIM**](cim-usbhub.md)
</dt> </dl>

 

