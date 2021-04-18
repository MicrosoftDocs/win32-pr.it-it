---
description: Rappresenta il Trusted Platform Module (TPM), un chip di sicurezza hardware che fornisce una radice di attendibilità per un sistema di computer.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316630"
---
# <a name="win32_tpm-class"></a>\_Classe TPM Win32

La **classe \_ TPM Win32** rappresenta il Trusted Platform Module (TPM), un chip di sicurezza hardware che fornisce una radice di attendibilità per un sistema di computer.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a>Members

La **classe \_ TPM Win32** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ TPM Win32** presenta questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBlockedCommand**](addblockedcommand-win32-tpm.md)                                 | Aggiunge un comando TPM all'elenco locale dei comandi bloccati in Windows.<br/>                                                                                                             |
| [**ChangeOwnerAuth**](changeownerauth-win32-tpm.md)                                     | Modifica il valore di autorizzazione del proprietario del TPM.<br/>                                                                                                                                       |
| [**Deselezionare**](clear-win32-tpm.md)                                                         | Reimposta il TPM sullo stato predefinito della factory.<br/>                                                                                                                                     |
| [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md)                               | Converte una passphrase fornita dall'utente in un valore di autorizzazione proprietario di 20 byte che può essere utilizzato per interagire con il TPM.<br/>                                                            |
| [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)                   | Crea una coppia di chiavi di approvazione a 2048 bit nel TPM.<br/>                                                                                                                              |
| [**Disabilita**](disable-win32-tpm.md)                                                     | Consente al proprietario del TPM di disabilitare il TPM.<br/>                                                                                                                                         |
| [**Abilitare**](enable-win32-tpm.md)                                                       | Consente al proprietario del TPM di abilitare il TPM.<br/>                                                                                                                                          |
| [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)               | Ottiene e restituisce l'operazione di presenza fisica del TPM in sospeso. Usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.<br/> |
| [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)             | Ottiene e restituisce i risultati di un'operazione di presenza fisica TPM eseguita.<br/>                                                                                          |
| [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)         | Indica l'azione dell'utente necessaria per eseguire un'operazione di presenza fisica del TPM.<br/>                                                                                           |
| [**IsActivated**](isactivated-win32-tpm.md)                                             | Indica se il TPM è attivato.<br/>                                                                                                                                          |
| [**IsCommandBlocked**](iscommandblocked-win32-tpm.md)                                   | Indica se il comando TPM può essere eseguito in questo sistema operativo.<br/>                                                                                                              |
| [**IsCommandPresent**](iscommandpresent-win32-tpm.md)                                   | Indica se un comando TPM è supportato da questo computer.<br/>                                                                                                                   |
| [**IsEnabled**](isenabled-win32-tpm.md)                                                 | Indica se il TPM è abilitato.<br/>                                                                                                                                            |
| [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md)             | Indica se il TPM ha una coppia di chiavi di verifica dell'autenticità.<br/>                                                                                                                           |
| [**Proprietario**](isowned-win32-tpm.md)                                                     | Indica se il TPM ha un proprietario.<br/>                                                                                                                                          |
| [**IsOwnerClearDisabled**](isownercleardisabled-win32-tpm.md)                           | Indica se il proprietario del TPM può cancellare il TPM.<br/>                                                                                                                               |
| [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)                               | Indica se è possibile installare un proprietario del TPM.<br/>                                                                                                                                  |
| [**IsPhysicalClearDisabled**](isphysicalcleardisabled-win32-tpm.md)                     | Indica se un'operazione di presenza fisica TPM può cancellare il TPM.<br/>                                                                                                           |
| [**IsPhysicalPresenceHardwareEnabled**](isphysicalpresencehardwareenabled-win32-tpm.md) | Indica se il computer supporta un percorso hardware dedicato per segnalare la presenza fisica.<br/>                                                                                  |
| [**IsSrkAuthCompatible**](issrkauthcompatible-win32-tpm.md)                             | Indica se l'autorizzazione della chiave radice di archiviazione (SRK) è compatibile con Windows.<br/>                                                                                           |
| [**RemoveBlockedCommand**](removeblockedcommand-win32-tpm.md)                           | Rimuove un comando TPM dall'elenco locale di comandi bloccati da Windows.<br/>                                                                                                        |
| [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)                                   | Reimposta il periodo di timeout o un altro meccanismo che i produttori di TPM implementano per proteggersi dagli attacchi del dizionario sul TPM.<br/>                                                 |
| [**ResetSrkAuth**](resetsrkauth-win32-tpm.md)                                           | Reimposta il valore di autorizzazione della chiave radice di archiviazione (SRK) in modo che sia compatibile con Windows.<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | Esegue un test automatico del TPM e restituisce il risultato.<br/>                                                                                                                          |
| [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)               | Richiede l'esecuzione di un'operazione di presenza fisica TPM.<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | Installa un proprietario per il TPM.<br/>                                                                                                                                                   |



 

### <a name="properties"></a>Proprietà

La **classe \_ TPM Win32** dispone di queste proprietà.

<dl> <dt>

**\_InitialValue disattivato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il TPM è attivato.

**true** se il dispositivo è attivato (ovvero se **\_ InitialValue** è true); in caso contrario, **false**.

Questo valore viene archiviato quando viene creata un'istanza della classe. È possibile che il TPM modifichi lo stato tra la creazione dell'istanza e quando si seleziona questo valore. Per verificare se il TPM è attivato in tempo reale, usare il metodo [**disattivato**](isactivated-win32-tpm.md) .

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile.

</dd> <dt>

**IsEnabled \_ InitialValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il TPM è abilitato.

**true** se il dispositivo è abilitato (ovvero se **IsEnabled \_ InitialValue** è true); in caso contrario, **false**.

Questo valore viene archiviato quando viene creata un'istanza della classe. È possibile che il TPM modifichi lo stato tra la creazione dell'istanza e quando si seleziona questo valore. Per verificare se il TPM è abilitato in tempo reale, usare il metodo [**IsEnabled**](isenabled-win32-tpm.md) .

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile.

</dd> <dt>

**InitialValue di proprietà \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il TPM ha un proprietario.

**true** se il dispositivo ha un proprietario (ovvero se **\_ InitialValue** è true); in caso contrario, **false**.

Questo valore viene archiviato quando viene creata un'istanza della classe. È possibile che il TPM modifichi lo stato tra la creazione dell'istanza e quando si seleziona questo valore. Per verificare se il TPM è di proprietà in tempo reale, utilizzare il metodo di [**Proprietà**](isowned-win32-tpm.md) .

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile.

</dd> <dt>

**ManufacturerId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Informazioni di identificazione che denominano in modo univoco il produttore del TPM.

Quando i dati non sono disponibili, viene restituito zero.

Questo valore integer può essere convertito in un valore stringa interpretando ogni byte come carattere ASCII. Ad esempio, un valore intero di 1414548736 può essere suddiviso in questi 4 byte: 0x54, 0x50, irreversibile 0x4D e 0x00. Supponendo che la stringa venga interpretata da sinistra a destra, questo valore intero viene convertito in un valore stringa di "TPM".

</dd> <dt>

**ManufacturerVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del TPM, come specificato dal produttore.

Quando i dati non sono disponibili, viene restituito "non supportato".

</dd> <dt>

**ManufacturerVersionInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altre informazioni sulla versione specifiche del produttore per il TPM.

Quando i dati non sono disponibili, viene restituito "non supportato".

</dd> <dt>

**PhysicalPresenceVersionInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La versione dell'interfaccia di presenza fisica, un meccanismo di comunicazione utilizzato per eseguire le operazioni del dispositivo che richiedono la presenza fisica, supportata dal computer.

Questa interfaccia deve essere disponibile per l'esecuzione di operazioni di presenza fisica TPM. I **metodi \_ TPM Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)e [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) espongono le funzionalità dell'interfaccia di presenza fisica.

Quando i dati non sono disponibili, viene restituito "non supportato".

</dd> <dt>

**Versione specifica**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione della specifica del Trusted Computing Group (TCG) supportata dal TPM. Questo valore include la versione delle specifiche TCG principale e secondaria, il livello di revisione della specifica e il livello di revisione degli errori. Tutti i valori sono in formato esadecimale. Ad esempio, le informazioni sulla versione "1,2, 2, 0" indicano che il dispositivo è stato implementato nella specifica TCG versione 1,2, livello Revisione 2 e senza errori.

Quando i dati non sono disponibili, viene restituito "non supportato".

</dd> </dl>

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



 

 
