---
description: Imposta il descrittore di sicurezza per lo spazio dei nomi a cui è connesso un utente. Questo metodo richiede un descrittore di sicurezza in formato di matrice di byte binario. Se si scrive uno script, usare il metodo SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Metodo SetD della classe __SystemSecurity
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
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313208"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Metodo SetD della \_ \_ classe SystemSecurity

Il metodo **SetD** imposta il descrittore di sicurezza per lo spazio dei nomi a cui un utente è connesso. Questo metodo richiede un descrittore di sicurezza in formato di matrice di byte binario. Se si scrive uno script, usare il metodo [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) . Per ulteriori informazioni, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

Se si sta programmando in C++, è possibile modificare il descrittore di sicurezza binario usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e i metodi di conversione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Un utente deve disporre dell'autorizzazione per la **scrittura dell' \_ applicazione livello dati** e, per impostazione predefinita, un amministratore dispone di tale autorizzazione. L'unica parte del descrittore di sicurezza utilizzata è la voce di controllo di accesso (ACE) non ereditata nell'elenco di controllo di accesso discrezionale (DACL). Impostando il flag di **\_ ereditarietà del contenitore** nelle voci ACE, il descrittore di sicurezza interessa gli spazi dei nomi figlio. Sono consentite entrambe le voci ACE Allow e Deny.

> [!Note]  
> Poiché le voci ACE Deny e allow sono entrambe consentite in un DACL, l'ordine delle voci ACE è importante. Per ulteriori informazioni, vedere [ordinamento delle voci ACE in un DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

## <a name="syntax"></a>Sintassi


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SD* \[ in\]
</dt> <dd>

Matrice di byte che costituisce il descrittore di sicurezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** che indica lo stato di una chiamata al metodo. Per gli script e le applicazioni Visual Basic, il risultato può essere ottenuto da [OutParameters. returnValue](parsing-outparameters-objects.md). Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

Nell'elenco seguente sono elencati i valori restituiti significativi per i **set**.

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

Tentativo di eseguire questo metodo su un sistema operativo che non lo supporta.

</dd> <dt>

**\_oggetto WBEM E \_ non valido \_**
</dt> <dd>

SD non supera i test di validità di base.

</dd> <dt>

**\_parametro WBEM E \_ non valido \_**
</dt> <dd>

SD non è valido a causa di uno dei seguenti elementi:

-   DACL mancante.
-   DACL non valido.
-   Per ACE è stato impostato il flag del Rep per la **\_ \_ \_ scrittura completa WBEM** e il flag **del \_ \_ provider** di scrittura WBEM **\_ parzialmente \_ \_** o WBEM non è impostato.
-   Il flag ACE ereditato da ACE è impostato **\_ solo \_** se il **contenitore eredita il flag \_ \_ ACE** .
-   Per ACE è impostato un bit di accesso sconosciuto.
-   La voce ACE contiene un flag impostato che non è presente nella tabella.
-   ACE ha un tipo non presente nella tabella.
-   Proprietario e gruppo mancanti da SD.

Per ulteriori informazioni sui flag ACE (Access Control Entry), vedere [costanti di sicurezza WMI](wmi-security-constants.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sulla modifica della sicurezza dello spazio dei nomi a livello di programmazione o manuale, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Esempio

Nello script seguente viene illustrato come utilizzare **SetD** per impostare il descrittore di sicurezza dello spazio dei nomi per lo spazio dei nomi radice e modificarlo nella matrice di byte mostrata in *strSD*.


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



Nell'esempio di codice C# riportato di seguito viene usato System. Security. AccessControl. RawSecurityDescriptor per enumerare, inserire e rimuovere nuovi oggetti CommonAce in RawSecurityDescriptor. DiscretionaryAcl, quindi convertirli nuovamente in una matrice di byte per salvarli tramite SetD. È possibile recuperare un oggetto SecurityIdentifier usando NTAccount e translate.


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

[**\_\_SystemSecurity:: GetSd**](--systemsecurity-getsd.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

