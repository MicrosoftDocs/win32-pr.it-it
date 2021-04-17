---
title: Metodo CreateRestorePoint della classe SystemRestore
description: Crea un punto di ripristino.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Ripristino del sistema del metodo CreateRestorePoint
- Ripristino del sistema del metodo CreateRestorePoint, classe SystemRestore
- SystemRestore Class System Restore, metodo CreateRestorePoint
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477146"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a>Metodo CreateRestorePoint della classe SystemRestore

Crea un punto di ripristino.

Questo metodo è l'equivalente tramite script della funzione [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrizione* \[ di in\]
</dt> <dd>

Descrizione da visualizzare in modo che l'utente possa identificare facilmente un punto di ripristino. La lunghezza massima di una stringa ANSI è MAX \_ desc. La lunghezza massima di una stringa Unicode è MAX \_ desc \_ W. Per ulteriori informazioni, vedere il [testo della descrizione del punto di ripristino](restore-point-description-text.md).

</dd> <dt>

*RestorePointType* \[ in\]
</dt> <dd>

Tipo di punto di ripristino. Il membro può essere uno dei valori seguenti.



| Tipo di punto di ripristino                                                                                                                                                                                                                             | Significato                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Applicazione \_ di INSTALLARE**</dt> <dt>0</dt> </dl>         | È stata installata un'applicazione.<br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Applicazione \_ di Disinstalla**</dt> <dt>1</dt> </dl>   | Un'applicazione è stata disinstallata.<br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Dispositivo \_ \_Installazione driver**</dt> <dt>10</dt> </dl> | È stato installato un driver di dispositivo.<br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Modifica \_ di IMPOSTAZIONI**</dt> <dt>12</dt> </dl>                    | Sono state aggiunte o rimosse funzionalità per un'applicazione.<br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> Operazione <dt>**annullata \_ OPERAZIONE**</dt> <dt>13</dt> </dl>        | Un'applicazione deve eliminare il punto di ripristino creato. Ad esempio, un'applicazione utilizzerebbe questo flag quando un utente annulla un'installazione.<br/> |



 

</dd> <dt>

*EventType* \[ in\]
</dt> <dd>

Tipo di evento. Il membro può essere uno dei valori seguenti.



| Tipo di evento                                                                                                                                                                                                                                                      | Significato                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Inizia \_ \_ \_ Modifica del sistema annidato**</dt> <dt>102</dt> </dl> | Una modifica del sistema è iniziata. Una chiamata nidificata successiva non crea un nuovo punto di ripristino. <br/> Le chiamate successive devono utilizzare la modifica finale del \_ sistema annidato \_ \_ , non la \_ modifica del sistema finale \_ .<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Inizia \_ \_Modifica del sistema**</dt> <dt>100</dt> </dl>                       | Una modifica del sistema è iniziata. <br/> Una chiamata successiva deve utilizzare la \_ modifica del sistema finale \_ , non la modifica finale del \_ sistema annidato \_ \_ .<br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Fine \_ \_ \_ Modifica del sistema annidato**</dt> <dt>103</dt> </dl>       | Una modifica del sistema è terminata.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Fine \_ \_Modifica del sistema**</dt> <dt>101</dt> </dl>                             | Una modifica del sistema è terminata.<br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK. In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.

## <a name="remarks"></a>Commenti

* * Windows 8: * *

Una nuova chiave del registro di sistema consente agli sviluppatori di applicazioni di modificare la frequenza di creazione di punti di ripristino.

Le applicazioni devono creare questa chiave per utilizzarla perché non sarà preesistente nel sistema. Per impostazione predefinita, verranno applicati gli elementi seguenti se la chiave non esiste. Se un'applicazione chiama il metodo **createrestorepoint** per creare un punto di ripristino, Windows ignora la creazione di questo nuovo punto di ripristino se sono stati creati punti di ripristino nelle ultime 24 ore. Il metodo **createrestorepoint** restituisce **S \_ OK**.

Gli sviluppatori possono scrivere applicazioni che creano il valore **DWORD** **SystemRestorePointCreationFrequency** nella chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. Il valore di questa chiave del registro di sistema può modificare la frequenza di creazione del punto di ripristino. Il valore di questa chiave del registro di sistema può modificare la frequenza di creazione del punto di ripristino.

Se l'applicazione chiama **createrestorepoint** per creare un punto di ripristino e il valore della chiave del registro di sistema è 0, ripristino configurazione di sistema non ignora la creazione del nuovo punto di ripristino.

Se l'applicazione chiama **createrestorepoint** per creare un punto di ripristino e il valore della chiave del registro di sistema è Integer N, ripristino configurazione di sistema ignora la creazione di un nuovo punto di ripristino se sono stati creati punti di ripristino nei precedenti N minuti.

## <a name="examples"></a>Esempio


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
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

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





