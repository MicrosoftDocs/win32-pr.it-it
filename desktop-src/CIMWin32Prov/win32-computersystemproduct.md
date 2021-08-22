---
description: Rappresenta un prodotto. Sono inclusi il software e l'hardware usati in questo sistema informatico.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Win32_ComputerSystemProduct classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47312acde8f346ac4ac3b2260fe06a2a5270610f9b7265da2b627a4c92fb4b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119294031"
---
# <a name="win32_computersystemproduct-class"></a>Classe ComputerSystemProduct Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Win32 ComputerSystemProduct** rappresenta un prodotto. Sono inclusi il software e l'hardware usati in questo sistema informatico.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a>Members

La **classe \_ ComputerSystemProduct Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ComputerSystemProduct Win32** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale per il prodotto.

Questa proprietà viene ereditata da [**CIM \_ Product.**](cim-product.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale del prodotto.

Questa proprietà viene ereditata da [**CIM \_ Product.**](cim-product.md)

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.4")
</dt> </dl>

Identificazione del prodotto, ad esempio un numero di serie sul software, un numero dadi su un chip hardware o (per i prodotti non commerciali) un numero di progetto.

Questa proprietà viene ereditata da [**CIM \_ Product.**](cim-product.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.2")
</dt> </dl>

Nome del prodotto di uso comune.

Questa proprietà viene ereditata da [**CIM \_ Product.**](cim-product.md)

</dd> <dt>

**SKUNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Informazioni sull'unità di mantenimento delle scorte (SKU) del prodotto.

Questa proprietà viene ereditata da [**CIM \_ Product.**](cim-product.md)

</dd> <dt>

**UUID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("UUID di tipo SMBIOS \| \| 1")
</dt> </dl>

Identificatore univoco universale (UUID) per questo prodotto. Un UUID è un identificatore a 128 bit che è garantito essere diverso dagli altri UUID generati. Se un UUID non è disponibile, viene usato un UUID di tutti gli zeri.

Questo valore deriva dal **membro UUID** della **struttura System Information** nelle informazioni SMBIOS.

</dd> <dt>

**Fornitore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.1")
</dt> </dl>

Nome del fornitore del prodotto o dell'entità che vende il prodotto (produttore, rivenditore, OEM e così via).

Questa proprietà viene ereditata da [**CIM \_ Product.**](cim-product.md)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.3")
</dt> </dl>

Informazioni sulla versione del prodotto.

Questa proprietà viene ereditata da [**CIM \_ Product.**](cim-product.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ ComputerSystemProduct Win32** deriva da [**CIM \_ Product.**](cim-product.md)

## <a name="examples"></a>Esempio

LGet-BrokenHardware.ps1di PowerShell in TechNet Gallery usa **per Win32 \_ ComputerSystemProduct** per recuperare un elenco di hardware non funzionanti tramite WMI. [](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto \_ CIM**](cim-product.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

