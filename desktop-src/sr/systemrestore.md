---
title: Classe SystemRestore
description: Fornisce metodi per disabilitare e abilitare il monitoraggio, elencare i punti di ripristino disponibili e avviare un ripristino nel sistema locale.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Classe SystemRestore Ripristino configurazione di sistema
- Classe SystemRestore Ripristino configurazione di sistema , descritta
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca781f960f51c8f7804d56f3b2f5531517c3f16505f40dd48d442857fa58bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967990"
---
# <a name="systemrestore-class"></a>Classe SystemRestore

Fornisce metodi per disabilitare e abilitare il monitoraggio, elencare i punti di ripristino disponibili e avviare un ripristino nel sistema locale.

## <a name="syntax"></a>Sintassi

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a>Members

La **classe SystemRestore** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe SystemRestore** include questi metodi.



| Metodo                                                             | Descrizione                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Crea un punto di ripristino.<br/>                         |
| [**Disabilita**](disable-systemrestore.md)                           | Disabilita il monitoraggio in una determinata unità.<br/>       |
| [**Abilita**](enable-systemrestore.md)                             | Abilita il monitoraggio in una determinata unità.<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | Recupera lo stato dell'ultimo ripristino del sistema.<br/> |
| [**Restore**](restore-systemrestore.md)                           | Avvia un ripristino del sistema.<br/>                      |



 

### <a name="properties"></a>Proprietà

La **classe SystemRestore** ha queste proprietà.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Ora in cui si è verificata la modifica dello stato.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Descrizione da visualizzare in modo che l'utente possa identificare facilmente un punto di ripristino. La lunghezza massima di una stringa ANSI è MAX \_ DESC. La lunghezza massima di una stringa Unicode è MAX \_ DESC \_ W. Per altre informazioni, vedere [Testo della descrizione del punto di ripristino.](restore-point-description-text.md)

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Tipo di evento. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**BEGIN \_ MODIFICA \_ DI \_ SISTEMA ANNIDATA**</dt> <dt>102</dt> </dl> | È stata avviata una modifica del sistema. Una chiamata annidata successiva non crea un nuovo punto di ripristino. <br/> Le chiamate successive devono usare END \_ NESTED \_ SYSTEM \_ CHANGE, non END SYSTEM \_ \_ CHANGE.<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**BEGIN \_ MODIFICA \_ DI SISTEMA**</dt> <dt>100</dt> </dl>                       | È stata avviata una modifica del sistema.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**END \_ MODIFICA \_ DI \_ SISTEMA ANNIDATA**</dt> <dt>103</dt> </dl>       | È stata terminata una modifica di sistema.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**END \_ MODIFICA \_ DI SISTEMA**</dt> <dt>101</dt> </dl>                             | È stata terminata una modifica di sistema.<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Tipo di punto di ripristino. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**APPLICAZIONE \_ INSTALLARE**</dt> <dt>0</dt> </dl>         | È stata installata un'applicazione.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**APPLICAZIONE \_ DISINSTALLARE**</dt> <dt>1</dt> </dl>   | Un'applicazione è stata disinstallata.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**CANCELLED \_ OPERAZIONE**</dt> <dt>13</dt> </dl>        | Un'applicazione deve eliminare il punto di ripristino creato. Ad esempio, un'applicazione userebbe questo flag quando un utente annulla un'installazione. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**DISPOSITIVO \_ INSTALLAZIONE \_ DRIVER**</dt> <dt>10</dt> </dl> | È stato installato un driver di dispositivo.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**MODIFY \_ IMPOSTAZIONI**</dt> <dt>12</dt> </dl>                    | In un'applicazione sono state aggiunte o rimosse funzionalità.<br/>                                                                                                  |



 

</dd> <dt>

**Sequencenumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Numero di sequenza del punto di ripristino.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile ottenere un elenco di punti di ripristino usando il [**metodo SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) per recuperare una raccolta **di oggetti SystemRestore.** È possibile usare le proprietà della classe per identificare il punto di ripristino.

## <a name="examples"></a>Esempio

Lo script di esempio seguente enumera i punti di ripristino correnti.


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                         |
| Spazio dei nomi<br/>                | Root \\ Default<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

