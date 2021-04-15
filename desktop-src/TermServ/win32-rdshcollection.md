---
title: Classe Win32_RDSHCollection
description: Gestisce una raccolta di Desktop remoto host sessione.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDSHCollection Servizi Desktop remoto
- Classe Win32_RDSHCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477080"
---
# <a name="win32_rdshcollection-class"></a>Win32 \_ RDSHCollection (classe)

Gestisce una raccolta di Desktop remoto host sessione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDSHCollection** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDSHCollection** presenta questi metodi.



| Metodo                                                                      | Descrizione                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshcollection.md)           | Recupera un valore di proprietà Integer di un oggetto **Win32 \_ RDSHCollection** .<br/>                                                                                                                  |
| [**GetStringProperty**](getstringproperty-win32-rdshcollection.md)         | Recupera un valore della proprietà di stringa di un oggetto **Win32 \_ RDSHCollection** .<br/>                                                                                                                    |
| [**KeyValueCompareAndSet**](win32-rdshcollection-keyvaluecompareandset.md) | Confronta la chiave specificata nella raccolta con un comparand; Se corrispondono, la chiave viene impostata su un nuovo valore. Se la chiave non esiste, il metodo inserirà la chiave nella raccolta.<br/> |
| [**KeyValueDelete**](win32-rdshcollection-keyvaluedelete.md)               | Elimina dalla raccolta la chiave specificata e il valore associato.<br/>                                                                                                                       |
| [**KeyValueGet**](win32-rdshcollection-keyvalueget.md)                     | Recupera il valore associato alla chiave specificata nella raccolta.<br/>                                                                                                                    |
| [**SetInt32Property**](setint32property-win32-rdshcollection.md)           | Aggiorna un valore della proprietà Integer di un oggetto **Win32 \_ RDSHCollection** .<br/>                                                                                                                    |
| [**SetStringProperty**](setstringproperty-win32-rdshcollection.md)         | Aggiorna il valore di una proprietà di stringa di un oggetto **Win32 \_ RDSHCollection** .<br/>                                                                                                                      |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ RDSHCollection** dispone di queste proprietà.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene e imposta l'alias della raccolta.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene e imposta la descrizione della raccolta.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il nome della raccolta.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**Windows server 2012 R2 e Windows server 2012:** Questa proprietà non è disponibile prima di Windows Server 2016.

Tipo della raccolta.

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Normale** (0)


</dt> <dd></dd> <dt>



 (2)


</dt> <dd>

Riservato

</dd> <dt>



 (3)


</dt> <dd>

Riservato

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Autopersonal** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider di Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

