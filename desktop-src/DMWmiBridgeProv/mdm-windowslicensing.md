---
title: Classe MDM_WindowsLicensing
description: La \_ classe MDM WindowsLicensing è progettata per scenari di gestione delle licenze correlati.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- Classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, descritta
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301470"
---
# <a name="mdm_windowslicensing-class"></a>MDM \_ WindowsLicensing (classe)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ WindowsLicensing** è progettata per scenari di gestione delle licenze correlati. Attualmente, l'ambito è limitato agli aggiornamenti dell'edizione dei dispositivi Windows 10 desktop e mobile, ad esempio Windows 10 Pro a Windows 10 Enterprise. Questo CSP offre inoltre la possibilità di attivare o modificare il codice Product Key dei dispositivi Windows 10 desktop.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a>Members

La classe **MDM \_ WindowsLicensing** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **MDM \_ WindowsLicensing** ha questi metodi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></td>
<td style="text-align: left;">Installa un codice Product Key per i dispositivi Windows 10 desktop. Non viene riavviato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></td>
<td style="text-align: left;">Metodo per verificare se il codice Product Key immesso può essere usato per l'aggiornamento di un'edizione, l'attivazione o la modifica di un codice Product Key di Windows 10 per i dispositivi desktop.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></td>
<td style="text-align: left;">Fornire una licenza per l'aggiornamento di un'edizione di dispositivi Windows 10 Mobile.<br/>
<blockquote>
[!Note]<br />
Questo processo di aggiornamento non richiede un riavvio del sistema.
</blockquote>
<br/> <br/> Il tipo di data è XML.<br/> L'operazione supportata è Execute.<br/>
<blockquote>
[!Important]<br />
Il contenuto del file di licenza XML deve essere preceduto da un carattere di escape, ovvero non dovrebbe essere semplicemente un XML copiato. in caso contrario, l'aggiornamento dell'edizione nei dispositivi Windows 10 Mobile avrà esito negativo. Per ulteriori informazioni sull'escape corretto del file di licenza XML, vedere la sezione 2,4 della <a href="https://www.w3.org/TR/xml/">specifica W3C XML</a>. Il file di licenza XML viene acquisito da Microsoft Volume Licensing Service Center. L'organizzazione deve disporre di un contratto multilicenza con Microsoft per accedere al portale.
</blockquote>
<br/> Di seguito sono riportati i percorsi di aggiornamento validi per l'edizione quando si usa questo nodo tramite un pacchetto MDM o di provisioning:
<ul>
<li>Windows 10 Mobileto Windows 10 Mobile Enterprise<br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></td>
<td style="text-align: left;">Attiva il dispositivo per l'esecuzione del codice Product Key e l'aggiornamento dell'edizione del client.
<blockquote>
[!Note]<br />
Questo processo di aggiornamento richiede un riavvio del sistema.
</blockquote>
<br/> <br/> L'operazione supportata è Execute.<br/> Quando viene effettuato il push di un codice Product Key da un server MDM a un dispositivo dell'utente, <strong>changepk.exe</strong> viene eseguito con il codice Product Key. Al termine, viene visualizzata una notifica all'utente che è disponibile una nuova edizione di Windows 10. L'utente può quindi riavviare il sistema manualmente o, dopo due ore, il dispositivo verrà riavviato automaticamente per completare l'aggiornamento. L'utente riceverà una notifica di promemoria 10 minuti prima del riavvio automatico.<br/> Al termine del riavvio del dispositivo, il processo di aggiornamento dell'edizione viene completato. L'utente riceverà una notifica dell'esito positivo dell'aggiornamento.
<blockquote>
[!Important]<br />
Se un altro criterio richiede un riavvio del sistema che si verifica quando <strong>changepk.exe</strong> è in esecuzione, l'aggiornamento dell'edizione avrà esito negativo.
</blockquote>
<br/> <br/> Se un codice Product Key viene immesso in un pacchetto di provisioning e l'utente inizia l'installazione del pacchetto, viene visualizzata una notifica per l'utente che il sistema verrà riavviato per completare l'installazione del pacchetto. Al momento del consenso esplicito da parte dell'utente, il pacchetto continua l'installazione e <strong>changepk.exe</strong> viene eseguito con il codice Product Key. L'utente riceverà una notifica di promemoria 30 secondi prima del riavvio automatico. <br/> Al termine del riavvio del dispositivo, il processo di aggiornamento dell'edizione viene completato. L'utente riceverà una notifica dell'esito positivo dell'aggiornamento. <br/> Questo nodo può essere usato anche per attivare o modificare un codice Product Key in un'edizione specifica del dispositivo desktop Windows 10 immettendo un codice Product Key. L'attivazione o la modifica di un codice Product Key non richiede un riavvio ed è un processo invisibile per l'utente.<br/>
<blockquote>
[!Important]<br />
Il codice Product Key immesso deve essere costituito da 29 caratteri, ovvero deve includere trattini. in caso contrario, l'attivazione, l'aggiornamento dell'edizione o la modifica del codice Product Key nei dispositivi desktop Windows 10 avranno esito negativo. Il codice Product Key viene acquisito da Microsoft Volume Licensing Service Center. L'organizzazione deve disporre di un contratto multilicenza con Microsoft per accedere al portale.
</blockquote>
<br/> Di seguito sono riportati i percorsi di aggiornamento validi per l'edizione quando si usa questo nodo tramite MDM:
<ul>
<li>Windows 10 Enterprise per Windows 10 Education</li>
<li>Windows 10 Home a Windows 10 Education</li>
<li>Windows 10 Pro a Windows 10 Education</li>
<li>Da Windows 10 Pro a Windows 10 Enterprise</li>
</ul>
<br/> L'attivazione o la modifica di un codice Product Key può essere eseguita nelle edizioni seguenti:
<ul>
<li>Windows 10 Education</li>
<li>Windows 10 Enterprise</li>
<li>Windows 10 Home</li>
<li>Windows 10 Pro</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Proprietà

La classe **MDM \_ WindowsLicensing** ha queste proprietà.

<dl> <dt>

[Edizione](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre.

</dd> <dt>

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/"

</dd> <dt>

[Status](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ DMMap MDM CIMv2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

