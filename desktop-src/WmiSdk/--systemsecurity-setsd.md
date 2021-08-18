---
description: Imposta il descrittore di sicurezza per lo spazio dei nomi a cui è connesso un utente. Questo metodo richiede un descrittore di sicurezza in formato matrice di byte binario. Se si scrive uno script, usare il metodo SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Metodo SetSD della __SystemSecurity classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 04da59b6370e2e9a381f2e3889b75ac37cb926e54c46cc0e616ec5353ed6f665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132034"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Metodo SetSD della \_ \_ classe SystemSecurity

Il **metodo SetSD imposta** il descrittore di sicurezza per lo spazio dei nomi a cui è connesso un utente. Questo metodo richiede un descrittore di sicurezza in formato matrice di byte binario. Se si scrive uno script, usare il [**metodo SetSecurityDescriptor.**](setsecuritydescriptor-method-in-class---systemsecurity.md) Per altre informazioni, vedere [Securing WMI Namespaces (Protezione degli spazi dei nomi WMI)](securing-wmi-namespaces.md) e Changing Access Security on Securable Objects (Modifica della [sicurezza degli accessi per gli oggetti a protezione diretta).](changing-access-security-on-securable-objects.md)

Se si programma in C++, è possibile modificare il descrittore di sicurezza binario usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e i metodi di conversione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Un utente deve disporre **dell'autorizzazione \_ WRITE DAC** e, per impostazione predefinita, un amministratore dispone di tale autorizzazione. L'unica parte del descrittore di sicurezza utilizzata è la voce di controllo di accesso (ACE) non ereditata nell'elenco di controllo di accesso discrezionale (DACL). Impostando il flag **CONTAINER \_ INHERIT** nelle voci ACE, il descrittore di sicurezza influisce sugli spazi dei nomi figlio. Sono consentite sia le ACE consentite che le ACE di negazione.

> [!Note]  
> Poiché le ACE deny e allow sono entrambe consentite in un elenco DACL, l'ordine delle ACE è importante. Per altre informazioni, vedere [Ordinamento di ACE in un DACL.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

 

## <a name="syntax"></a>Sintassi


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SD* \[ Pollici\]
</dt> <dd>

Matrice di byte che costituisce il descrittore di sicurezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **HRESULT** che indica lo stato di una chiamata al metodo. Per script e Visual Basic applicazioni, il risultato può essere ottenuto da [OutParameters.ReturnValue](parsing-outparameters-objects.md). Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

Nell'elenco seguente sono elencati i valori restituiti significativi per **SetSD**.

<dl> <dt>

**S \_ OK**
</dt> <dd>

Metodo eseguito correttamente.

</dd> <dt>

**ACCESSO WBEM \_ E \_ \_ NEGATO**
</dt> <dd>

Il chiamante non dispone di diritti sufficienti per chiamare questo metodo.

</dd> <dt>

**METODO WBEM \_ E \_ \_ DISABILITATO**
</dt> <dd>

Si è tentato di eseguire questo metodo nel sistema operativo che non lo supporta.

</dd> <dt>

**OGGETTO WBEM \_ E \_ NON \_ VALIDO**
</dt> <dd>

SD non supera i test di validità di base.

</dd> <dt>

**PARAMETRO WBEM \_ E \_ NON \_ VALIDO**
</dt> <dd>

SD non è valido a causa di una delle condizioni seguenti:

-   DACL mancante.
-   DACL non valido.
-   ACE ha il flag **\_ WBEM FULL WRITE \_ \_ REP** impostato e il flag **WBEM \_ PARTIAL WRITE \_ \_ REP** o **WBEM \_ WRITE \_ PROVIDER** non è impostato.
-   ACE ha il flag **INHERIT \_ ONLY \_ ACE** impostato senza il flag **CONTAINER INHERIT \_ \_ ACE.**
-   ACE ha un set di bit di accesso sconosciuto.
-   ACE ha un flag impostato che non è presente nella tabella.
-   ACE ha un tipo che non è presente nella tabella.
-   Il proprietario e il gruppo non sono presenti nella DS.

Per altre informazioni sui flag ACE (Access Control Entry), vedere [Costanti di sicurezza WMI.](wmi-security-constants.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Per altre informazioni sulla modifica della sicurezza dello spazio dei nomi a livello di codice o manualmente, vedere [Protezione degli spazi dei nomi WMI.](securing-wmi-namespaces.md)

## <a name="examples"></a>Esempio

Lo script seguente illustra come usare **SetSD** per impostare il descrittore di sicurezza dello spazio dei nomi radice e modificarlo nella matrice di byte illustrata in *strSD*.


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



L'esempio di codice C# seguente usa System.Security.AccessControl.RawSecurityDescriptor per enumerare, inserire e rimuovere nuovi oggetti CommonAce in RawSecurityDescriptor.DiscretionaryAcl e quindi riconvertirlo in una matrice di byte per salvarlo tramite SetSD. Un SecurityIdentifier può essere recuperato usando NTAccount e Translate.


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

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

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

