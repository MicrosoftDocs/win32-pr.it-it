---
description: Questa classe è deprecata. È invece consigliabile derivare dalla classe di servizio \_ CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService classe
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
ms.openlocfilehash: cfb2ea7b122516cc3b62f675684649e22577171f713856638f97985d9713e8d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694691"
---
# <a name="cim_networkservice-class"></a>Classe CiM \_ NetworkService

Questa classe è deprecata. È invece consigliabile derivare dalla [**classe di servizio CIM. \_**](cim-service.md)

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

La **classe CIM \_ NetworkService** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ NetworkService** ha queste proprietà.

<dl> <dt>

**Parole chiave**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Nessun valore")
</dt> </dl>

Questa proprietà è deprecata e non deve essere usata.

> [!Note]  
> Descrizione deprecata: matrice di parole chiave che possono essere usate nelle query.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Questa proprietà è deprecata. È invece consigliabile usare la **classe \_ CIM ServiceAccessURI.**

> [!Note]  
> Descrizione deprecata: URL che fornisce il protocollo, il percorso di rete e altre informazioni specifiche del servizio necessarie per accedere al servizio.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Nessun valore")
</dt> </dl>

Questa proprietà è deprecata e non deve essere usata.

> [!Note]  
> Descrizione deprecata: le pre-condizioni che devono essere soddisfatte per consentire il corretto avvio del servizio.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Nessun valore")
</dt> </dl>

Questa proprietà è deprecata e non deve essere usata.

> [!Note]  
> Descrizione deprecata: parametri che devono essere forniti al metodo **StartService** per consentire l'avvio corretto del servizio.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ CIM**](cim-service.md)
</dt> </dl>

 

