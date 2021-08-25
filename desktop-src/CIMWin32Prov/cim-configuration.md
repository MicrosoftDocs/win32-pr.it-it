---
description: L'oggetto Configurazione CIM consente il raggruppamento di set di parametri (definiti negli oggetti Impostazione CIM) e dipendenze per uno o \_ più elementi di sistema \_ gestiti.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: CIM_Configuration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c6df2338d46438bf3e1af371ebbce8b36f1a337f26a4785064119cca45bece46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924931"
---
# <a name="cim_configuration-class"></a>Classe di configurazione \_ CIM

**L'oggetto \_ Configurazione CIM** consente il raggruppamento di set di parametri (definiti negli oggetti [**\_ Impostazione CIM)**](cim-setting.md) e dipendenze per uno o più elementi di sistema gestiti. Questo oggetto rappresenta un determinato comportamento o uno stato funzionale desiderato per gli elementi di sistema gestiti. Lo stato funzionale desiderato è in genere basato su requisiti esterni, ad esempio ora o posizione. Ad esempio, per connettersi a un sistema di posta elettronica da casa, esiste una dipendenza da un modem; mentre esiste una dipendenza da una scheda di rete. Impostazioni per i dispositivi logici pertinenti (in questo esempio, modem e scheda di rete POTS) possono essere definiti e aggregati dalla configurazione **CIM \_**. È quindi possibile definire due configurazioni Connessione alla posta elettronica raggruppando le dipendenze pertinenti e gli [**oggetti \_ impostazione CIM.**](cim-setting.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Members

La **classe Configuration \_ di CIM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Configuration \_ di CIM** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale **dell'oggetto \_ Configurazione CIM.**

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale **dell'oggetto \_ Configurazione CIM.**

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Etichetta con cui è **noto l'oggetto \_ Configurazione CIM.**

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

