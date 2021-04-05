---
title: Classe SystemRestore
description: Fornisce metodi per disabilitare e abilitare il monitoraggio, elencare i punti di ripristino disponibili e avviare un ripristino nel sistema locale.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Ripristino del sistema della classe SystemRestore
- Ripristino del sistema della classe SystemRestore, descritto
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
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048487"
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

La classe **SystemRestore** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **SystemRestore** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Crea un punto di ripristino.<br/>                         |
| [**Disabilita**](disable-systemrestore.md)                           | Disabilita il monitoraggio in un'unità specifica.<br/>       |
| [**Abilitare**](enable-systemrestore.md)                             | Abilita il monitoraggio in un'unità specifica.<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | Recupera lo stato dell'ultimo ripristino di sistema.<br/> |
| [**Restore**](restore-systemrestore.md)                           | Avvia un ripristino di sistema.<br/>                      |



 

### <a name="properties"></a>Proprietà

La classe **SystemRestore** dispone di queste proprietà.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ora in cui si è verificata la modifica dello stato.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Descrizione da visualizzare in modo che l'utente possa identificare facilmente un punto di ripristino. La lunghezza massima di una stringa ANSI è MAX \_ desc. La lunghezza massima di una stringa Unicode è MAX \_ desc \_ W. Per ulteriori informazioni, vedere il [testo della descrizione del punto di ripristino](restore-point-description-text.md).

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Tipo di evento. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Inizia \_ \_ \_ Modifica del sistema annidato**</dt> <dt>102</dt> </dl> | Una modifica del sistema è iniziata. Una chiamata nidificata successiva non crea un nuovo punto di ripristino. <br/> Le chiamate successive devono utilizzare la modifica finale del \_ sistema annidato \_ \_ , non la \_ modifica del sistema finale \_ .<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Inizia \_ \_Modifica del sistema**</dt> <dt>100</dt> </dl>                       | Una modifica del sistema è iniziata.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Fine \_ \_ \_ Modifica del sistema annidato**</dt> <dt>103</dt> </dl>       | Una modifica del sistema è terminata.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Fine \_ \_Modifica del sistema**</dt> <dt>101</dt> </dl>                             | Una modifica del sistema è terminata.<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Tipo di punto di ripristino. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Applicazione \_ di INSTALLARE**</dt> <dt>0</dt> </dl>         | È stata installata un'applicazione.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Applicazione \_ di Disinstalla**</dt> <dt>1</dt> </dl>   | Un'applicazione è stata disinstallata.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> Operazione <dt>**annullata \_ OPERAZIONE**</dt> <dt>13</dt> </dl>        | Un'applicazione deve eliminare il punto di ripristino creato. Ad esempio, un'applicazione utilizzerebbe questo flag quando un utente annulla un'installazione. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Dispositivo \_ \_Installazione driver**</dt> <dt>10</dt> </dl> | È stato installato un driver di dispositivo.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Modifica \_ di IMPOSTAZIONI**</dt> <dt>12</dt> </dl>                    | Sono state aggiunte o rimosse funzionalità per un'applicazione.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Numero di sequenza del punto di ripristino.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile ottenere un elenco di punti di ripristino usando il metodo [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) per recuperare una raccolta di oggetti **SystemRestore** . È possibile utilizzare le proprietà della classe per identificare il punto di ripristino.

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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                         |
| Spazio dei nomi<br/>                | \\Impostazioni predefinite radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

