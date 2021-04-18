---
description: Questa classe è deprecata. È invece consigliabile derivare dalla classe del \_ servizio CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Classe CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317214"
---
# <a name="cim_networkservice-class"></a>\_Classe CIM NetworkService

Questa classe è deprecata. È invece consigliabile derivare dalla classe [**del \_ servizio CIM**](cim-service.md) .

## <a name="syntax"></a>Sintassi

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a>Members

La classe **CIM \_ NetworkService** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ NetworkService** dispone di queste proprietà.

<dl> <dt>

**Parole chiave**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")
</dt> </dl>

Questa proprietà è deprecata e non deve essere usata.

> [!Note]  
> Descrizione deprecata: matrice di parole chiave che può essere utilizzata nelle query.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Questa proprietà è deprecata. È invece consigliabile usare la classe **CIM \_ ServiceAccessURI** .

> [!Note]  
> Descrizione deprecata: un URL che fornisce il protocollo, il percorso di rete e altre informazioni specifiche del servizio necessarie per accedere al servizio.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")
</dt> </dl>

Questa proprietà è deprecata e non deve essere usata.

> [!Note]  
> Descrizione deprecata: le condizioni preliminari che devono essere soddisfatte affinché il servizio venga avviato correttamente.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")
</dt> </dl>

Questa proprietà è deprecata e non deve essere usata.

> [!Note]  
> Deprecated Description: parametri che devono essere forniti al metodo **StartService** per poter avviare correttamente il servizio.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio CIM**](cim-service.md)
</dt> </dl>

 

