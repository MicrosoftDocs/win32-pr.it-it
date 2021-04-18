---
description: Ottiene il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente. Questo metodo restituisce un descrittore di sicurezza in formato di matrice di byte binario. Se si scrive uno script, usare il metodo GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Metodo ottenuto della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313210"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a>Metodo ottenuto della \_ \_ classe SystemSecurity

Il metodo **getsd** ottiene il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente. Questo metodo restituisce un descrittore di sicurezza in formato di matrice di byte binario. Se si scrive uno script, usare il metodo [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) . Per ulteriori informazioni, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

L'utente deve disporre dell' **autorizzazione \_ controllo lettura** . Per impostazione predefinita, gli amministratori dispongono di tale autorizzazione. L'unica parte del descrittore di sicurezza effettivamente utilizzato è l'elenco di controllo di accesso discrezionale (DACL). L'elenco DACL può contenere sia voci ACE ereditate che non ereditate. Sono consentite le voci ACE Deny e Allow.

Se si sta programmando in C++, è possibile modificare il descrittore di sicurezza binario usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e i metodi di conversione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="syntax"></a>Sintassi


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SD* \[ out\]
</dt> <dd>

Descrittore di sicurezza nel formato di matrice di byte binario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **HRESULT** che indica lo stato della chiamata al metodo. Nell'elenco seguente sono elencati i valori restituiti che sono di importanza per **ottenere**. Per gli script e le applicazioni Visual Basic, il risultato può essere ottenuto da [OutParameters. returnValue](parsing-outparameters-objects.md). Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_OK**
</dt> <dd>

Il metodo è stato eseguito correttamente.

</dd> <dt>

**accesso a WBEM \_ E \_ \_ negato**
</dt> <dd>

Il chiamante non dispone di diritti sufficienti per chiamare questo metodo.

</dd> <dt>

**WBEM \_ E \_ metodo \_ disabilitato**
</dt> <dd>

Tentativo di eseguire questo metodo su un sistema non supportato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sulla modifica della sicurezza dello spazio dei nomi a livello di programmazione o manuale, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Esempio

Nello script seguente viene illustrato **come utilizzare il** metodo per ottenere il descrittore di sicurezza corrente per lo \\ spazio dei nomi Cimv2 radice e modificarlo nella matrice di byte visualizzata in **displayd**.


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_\_SystemSecurity:: SetD**](--systemsecurity-setsd.md)
</dt> <dt>

[**Descrittore di sicurezza \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

