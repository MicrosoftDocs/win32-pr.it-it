---
description: Consente a un client di gestire le impostazioni della quota disco globale di un volume NTFS. Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia DIDiskQuotaUser per gli script e le applicazioni basate Visual Basic Microsoft.
title: Oggetto DIDiskQuotaUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843242"
---
# <a name="didiskquotauser-object"></a>Oggetto DIDiskQuotaUser

Consente a un client di gestire le impostazioni della quota disco globale di un volume NTFS. Questo oggetto rende disponibili le funzionalità essenziali **dell'interfaccia DIDiskQuotaUser** per gli script e le applicazioni basate Visual Basic Microsoft.

## <a name="members"></a>Membri

**L'oggetto DIDiskQuotaUser** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto DIDiskQuotaUser** dispone di questi metodi.



| Metodo                                           | Descrizione                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**Invalidare**](didiskquotauser-invalidate.md) | Cancella le informazioni utente memorizzate nella cache dell'oggetto.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto DIDiskQuotaUser** ha queste proprietà.



| Proprietà                                                                        | Tipo di accesso           | Descrizione                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**AccountContainerName**](didiskquotauser-accountcontainername.md)<br/> | Sola lettura<br/>  | Ottiene il nome del contenitore di account dell'utente.<br/>                                            |
| [**AccountStatus**](didiskquotauser-accountstatus.md)<br/>               | Sola lettura<br/>  | Ottiene lo stato dell'account dell'utente.<br/>                                                    |
| [**Displayname**](didiskquotauser-displayname.md)<br/>                   | Sola lettura<br/>  | Ottiene il nome visualizzato dell'utente.<br/>                                                             |
| [**ID**](didiskquotauser-id.md)<br/>                                     | Sola lettura<br/>  | Ottiene un ID che identifica in modo univoco l'utente.<br/>                                             |
| [**LogonName**](didiskquotauser-logonname.md)<br/>                       | Sola lettura<br/>  | Ottiene il nome dell'account di accesso dell'utente.<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | Lettura/Scrittura<br/> | Imposta o ottiene il limite di quota corrente [**dell'utente.**](diskquotacontrol-object.md)<br/>           |
| [**QuotaLimitText**](didiskquotauser-quotalimittext.md)<br/>             | Sola lettura<br/>  | Ottiene il limite di quota corrente [**dell'utente**](diskquotacontrol-object.md) come stringa di testo. <br/> |
| [**QuotaThreshold**](didiskquotauser-quotathreshold.md)<br/>             | Lettura/Scrittura<br/> | Imposta o ottiene la soglia di avviso dell'utente, in byte.<br/>                                      |
| [**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)<br/>     | Sola lettura<br/>  | Ottiene la soglia di avviso dell'utente come stringa di testo.<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | Sola lettura<br/>  | Ottiene l'utilizzo corrente del disco dell'utente, in byte.<br/>                                             |
| [**QuotaUsedText**](didiskquotauser-quotausedtext.md)<br/>               | Sola lettura<br/>  | Ottiene l'utilizzo corrente del disco dell'utente come stringa di testo.<br/>                                      |



 

## <a name="remarks"></a>Commenti

A ogni utente del volume gestito dall'oggetto [**DiskQuotaControl**](diskquotacontrol-object.md) è associato un oggetto **DIDiskQuotaUser.** Questo oggetto consente a un client di gestire le impostazioni di un singolo utente. Esistono diversi modi per ottenere l'oggetto **DIDiskQuotaUser** di un utente:

-   Gli **oggetti DIDiskQuotaUser** per tutti gli utenti con quote nel volume vengono esposti come raccolta e possono essere enumerati. Di seguito viene descritto come **enumerare gli oggetti DIDiskQuotaUser.**
-   Quando si aggiunge un nuovo utente, il [**metodo AddUser**](diskquotacontrol-adduser.md) restituisce l'oggetto **DIDiskQuotaUser** dell'utente.
-   Se si ha il nome dell'utente, il [**metodo FindUser**](diskquotacontrol-finduser.md) restituisce l'oggetto **DIDiskQuotaUser** dell'utente.

### <a name="enumerating-disk-quota-users"></a>Enumerazione degli utenti della quota disco

Gli **oggetti DIDiskQuotaUser** per tutti gli utenti con una quota nel volume vengono esposti come raccolta. [**L'oggetto DiskQuotaControl**](diskquotacontrol-object.md) esporta un metodo enumeratore standard che consente di enumerare la raccolta di **oggetti DIDiskQuotaUser.** La procedura seguente illustra come eseguire l'enumerazione con Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262). È possibile usare una procedura simile con Visual Basic o Microsoft Visual Basic Scripting Edition (VBScript).

1.  Creare un nuovo [**oggetto DiskQuotaControl.**](diskquotacontrol-object.md)
2.  Inizializzarlo con [**Initialize**](diskquotacontrol-initialize.md).
3.  Creare un nuovo oggetto **Enumerator JScript.**
4.  Usare un **ciclo for** per enumerare gli **oggetti DIDiskQuotaUser.** Non è necessario impostare un valore iniziale. Il metodo **moveNext** dell'oggetto enumeratore notifica al **metodo item** di restituire l'oggetto **DIDiskQuotaUser** successivo. Il **metodo atEnd** restituisce **false** quando si raggiunge la fine dell'elenco.
5.  In base alle esigenze, usare l'oggetto **DIDiskQuotaUser** restituito dal metodo **item** dell'enumeratore per recuperare o impostare una o più proprietà della quota disco dell'utente associato.

Il frammento di codice seguente illustra come enumerare **gli oggetti DIDiskQuotaUser** con JScript. **\_ L'argomento Volume Label** passato alla funzione **EnumUsers** è un valore stringa contenente un'etichetta di volume, ad esempio "C:". \\ \\


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Shell**](shell.md)
</dt> </dl>

 

 




