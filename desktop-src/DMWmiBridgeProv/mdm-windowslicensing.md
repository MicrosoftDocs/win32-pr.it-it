---
title: MDM_WindowsLicensing classe
description: La classe \_ MDM WindowsLicensing è progettata per scenari di gestione correlati alle licenze.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing classe
- MDM_WindowsLicensing classe, descritta
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
ms.openlocfilehash: ca9470b72cb6a50323af9294be4a6506682fc7aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480927"
---
# <a name="mdm_windowslicensing-class"></a>Classe \_ MDM WindowsLicensing

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ MDM WindowsLicensing** è progettata per scenari di gestione correlati alle licenze. Attualmente l'ambito è limitato agli aggiornamenti dell'edizione di Windows 10 desktop e dispositivi mobili, ad esempio Windows 10 Pro a Windows 10 Enterprise. Inoltre, questo provider di servizi di configurazione offre la possibilità di attivare o modificare il codice Product Key Windows 10 dispositivi desktop.

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

La **classe \_ MDM WindowsLicensing** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ MDM WindowsLicensing** include questi metodi.




| Metodo | Descrizione | 
|--------|-------------|
| <a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a> | Installa un codice Product Key per i Windows 10 desktop. Non viene riavviato.<br /> | 
| <a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a> | Metodo per verificare se il codice Product Key immesso può essere usato per un aggiornamento dell'edizione, l'attivazione o la modifica di un codice Product Key Windows 10 per i dispositivi desktop.<br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>Metodo UpgradeEditionWithLicenseMethod</strong></a> | Fornire una licenza per un aggiornamento dell'edizione Windows 10 dispositivi mobili.<br /><blockquote>[!Note]<br />Questo processo di aggiornamento non richiede un riavvio del sistema.</blockquote><br /><br /> Il tipo di data è XML.<br /> L'operazione supportata è Execute.<br /><blockquote>[!Important]<br />Il contenuto del file di licenza XML deve essere preceduto da un carattere di escape corretto, ovvero non deve essere semplicemente un codice XML copiato, in caso contrario l'aggiornamento dell'edizione Windows 10 dispositivi mobili avrà esito negativo. Per altre informazioni sull'escape corretto del file di licenza XML, vedere la sezione 2.4 della <a href="https://www.w3.org/TR/xml/">specifica XML W3C</a>. Il file di licenza XML viene acquisito da Microsoft Volume Licensing Service Center. L'organizzazione deve avere un contratto multilicenza con Microsoft per accedere al portale.</blockquote><br /> Di seguito sono riportati i percorsi di aggiornamento dell'edizione validi quando si usa questo nodo tramite un pacchetto MDM o di provisioning:<ul><li>Windows 10 Mobileto Windows 10 Mobile Enterprise<br /></li></ul><br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>Metodo UpgradeEditionWithProductKeyMethod</strong></a> | Attiva il dispositivo per prendere il codice Product Key e aggiornare l'edizione del client.<blockquote>[!Note]<br />Questo processo di aggiornamento richiede un riavvio del sistema.</blockquote><br /><br /> L'operazione supportata è Execute.<br /> Quando viene eseguito il push di un codice Product Key da un server MDM al dispositivo di un <strong> utente, </strong>changepk.exeviene eseguito usando il codice Product Key. Al termine, viene visualizzata una notifica all'utente che è disponibile una nuova edizione di Windows 10. L'utente può quindi riavviare il sistema manualmente o, dopo due ore, il dispositivo verrà riavviato automaticamente per completare l'aggiornamento. L'utente riceverà una notifica di promemoria 10 minuti prima del riavvio automatico.<br /> Dopo il riavvio del dispositivo, il processo di aggiornamento dell'edizione viene completato. L'utente riceverà una notifica dell'esito positivo dell'aggiornamento.<blockquote>[!Important]<br />Se un altro criterio richiede un riavvio del sistema che si verifica <strong>changepk.exe</strong> è in esecuzione, l'aggiornamento dell'edizione avrà esito negativo.</blockquote><br /><br /> Se viene immesso un codice Product Key in un pacchetto di provisioning e l'utente inizia l'installazione del pacchetto, viene visualizzata una notifica all'utente che il sistema verrà riavviato per completare l'installazione del pacchetto. Dopo il consenso esplicito dell'utente a procedere, il pacchetto continua <strong> l'installazione echangepk.exe</strong> esecuzione usando il codice Product Key. L'utente riceverà una notifica di promemoria 30 secondi prima del riavvio automatico. <br /> Dopo il riavvio del dispositivo, il processo di aggiornamento dell'edizione viene completato. L'utente riceverà una notifica dell'esito positivo dell'aggiornamento. <br /> Questo nodo può essere usato anche per attivare o modificare un codice Product Key in una determinata edizione Windows 10 dispositivo desktop immettendo un codice Product Key. L'attivazione o la modifica di un codice Product Key non richiede un riavvio ed è un processo invisibile all'utente.<br /><blockquote>[!Important]<br />Il codice Product Key immesso deve essere di 29 caratteri, ovvero deve includere trattini, in caso contrario l'attivazione Windows 10, l'aggiornamento dell'edizione o la modifica del codice Product Key nei dispositivi desktop non riuscirà. Il codice Product Key viene acquisito da Microsoft Volume Licensing Service Center. L'organizzazione deve avere un contratto multilicenza con Microsoft per accedere al portale.</blockquote><br /> Di seguito sono riportati i percorsi di aggiornamento dell'edizione validi quando si usa questo nodo tramite MDM:<ul><li>Windows 10 Enterprise da Windows 10 Education</li><li>Windows 10 Home da Windows 10 Education</li><li>Windows 10 Pro da Windows 10 Education</li><li>Windows 10 Pro da Windows 10 Enterprise</li></ul><br /> L'attivazione o la modifica di un codice Product Key possono essere eseguite nelle edizioni seguenti:<ul><li>Windows 10 Education</li><li>Windows 10 Enterprise</li><li>Windows 10 Home</li><li>Windows 10 Pro</li></ul><br /> | 




 

### <a name="properties"></a>Proprietà

La **classe \_ MDM WindowsLicensing** ha queste proprietà.

<dl> <dt>

[Edizione](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre.

</dd> <dt>

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/"

</dd> <dt>

[Status](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | DMMap \\ MDM CIMv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

