---
title: Gestione degli eventi di acquisizione delle licenze
description: Gestione degli eventi di acquisizione delle licenze
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media Format SDK, gestione degli eventi di acquisizione delle licenze
- Windows Media Format SDK, eventi di acquisizione delle licenze
- Advanced Systems Format (ASF), gestione degli eventi di acquisizione delle licenze
- ASF (Advanced Systems Format), gestione degli eventi di acquisizione delle licenze
- Advanced Systems Format (ASF), eventi di acquisizione delle licenze
- ASF (Advanced Systems Format), eventi di acquisizione delle licenze
- digital rights management (DRM), gestione degli eventi di acquisizione delle licenze
- DRM (digital rights management), gestione degli eventi di acquisizione delle licenze
- digital rights management (DRM), eventi di acquisizione delle licenze
- DRM (digital rights management),eventi di acquisizione delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7eab9afe85d4e58ae422134e5268c5b411058cf5048f774994b0cc02b173fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006711"
---
# <a name="handling-license-acquisition-events"></a>Gestione degli eventi di acquisizione delle licenze

Un'applicazione di lettura abilitata per DRM, nel relativo metodo di callback [**IWMStatusCallback::OnStatus,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) gestisce i quattro eventi seguenti correlati al processo di acquisizione della licenza:

-   **STATO DELLA FIRMA \_ DI WMT \_ \_ LICENSEURL**
-   **NESSUN \_ DIRITTO WMT \_**
-   **WMT \_ NO \_ RIGHTS \_ EX**
-   **LICENZA DI ACQUISIZIONE \_ WMT \_**

**STATO DELLA FIRMA \_ DI WMT \_ \_ LICENSEURL**

Quando il componente DRM rileva il contenuto protetto da DRM versione 7, cerca innanzitutto una licenza valida nel sistema locale. Se non ne esiste nessuno, valuta l'URL di acquisizione della licenza nell'intestazione DRM del file e invia un evento **WMT \_ LICENSEURL \_ SIGNATURE \_ STATE** con *pValue* impostato su uno dei valori [**WMT \_ DRMLA \_ TRUST,**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) che indica se l'URL è attendibile, non attendibile o è stato manomesso. Se l'URL non è attendibile, l'applicazione dovrebbe avvisare l'utente. Se l'URL è stato manomesso, il file deve essere considerato danneggiato e l'applicazione non deve passare all'URL senza emettere un avviso sicuro all'utente.

**NESSUN \_ DIRITTO WMT \_**

**L'evento \_ NO \_ RIGHTS WMT** viene inviato solo per il contenuto DRM versione 1, il che significa che la licenza deve essere acquisita in modo non invisibile all'utente. In altre parole, l'utente deve passare a una pagina Web per acquisire una licenza. L'URL per la pagina viene recuperato come stringa con terminazione Null a caratteri wide dal *parametro pValue* nel **metodo OnStatus.**

Se appropriato, un'applicazione può rendere più semplice per l'utente passare alla pagina Web, aprendo Internet Explorer in un processo separato oppure ospitando il controllo Web Browser. Questa operazione non è tuttavia necessaria. Come minimo, un'applicazione potrebbe semplicemente visualizzare l'URL dell'utente in una finestra di messaggio e richiedergli di incollarlo nella barra degli indirizzi di Internet Explorer. L'esempio Audioplayer illustra la gestione corretta dell'evento **NO \_ \_ RIGHTS WMT,** incluso come formattare la stringa URL e come usare il metodo **CreateProcess** per aprire Internet Explorer e passare all'URL specificato.

Poiché l'applicazione non è in grado di sapere quando è stata acquisita una licenza DRM versione 1, l'utente deve tentare nuovamente di aprire il file dopo aver acquisito la licenza.

Questo stesso processo di acquisizione delle licenze non invisibile all'utente può essere usato anche per le licenze della versione 7, ma in questo caso l'applicazione può chiamare prima [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition). Questo metodo farà sì che l'archivio licenze locale sia controllato ripetutamente fino a quando non viene trovata la licenza per il nuovo file. A questo punto, l'applicazione riceverà un **evento WMT \_ ACQUIRE \_ LICENSE.** Per tutte le licenze della versione 7, è consigliabile che le applicazioni dia agli utenti la possibilità di ottenere le licenze in modo invisibile all'utente in modo invisibile all'utente.

**WMT \_ NO \_ RIGHTS \_ EX**

**L'evento WMT \_ NO RIGHTS \_ \_ EX** indica che il contenuto è protetto da DRM versione 7 e pertanto il processo di acquisizione della licenza può procedere in modalità invisibile all'utente o non invisibile all'utente. In generale, l'acquisizione delle licenze invisibile all'utente è più comoda per gli utenti finali, anche se alcuni utenti preferiscono acquisire tutte le licenze senza silenzio. Quando l'acquisizione della licenza richiede all'utente di inviare il pagamento o le informazioni personali, il processo deve sempre essere eseguito in modo non invisibile all'utente. L'acquisizione di licenze non invisibile all'utente è descritta in precedenza **nell'intestazione NO \_ RIGHTS \_ di WMT.** L'acquisizione invisibile all'utente procede come segue:

1.  Eseguire il *cast del parametro pValue* a una struttura [**WM GET LICENSE \_ \_ \_ DATA**](wm-get-license-data.md) e archiviare la struttura nel caso in cui sia necessaria in un secondo momento per l'acquisizione di licenze non invisibile all'utente.
2.  Chiamare **QueryInterface sull'oggetto** reader per ottenere [**l'interfaccia IWMDRMReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
3.  Chiamare [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) e specificare 0x1 nel *parametro dwFlags* per indicare l'acquisizione del linguaggio invisibile all'utente. Si tratta di una chiamata asincrona che restituisce immediatamente .
4.  Attendere **l'evento WMT \_ ACQUIRE \_ LICENSE.**

**LICENZA DI ACQUISIZIONE \_ WMT \_**

**L'evento WMT \_ ACQUIRE \_ LICENSE** viene inviato dopo il completamento del processo di acquisizione della licenza per una licenza DRM versione 7. [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causa l'invio dell'evento per l'acquisizione invisibile all'utente e [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) ne determina l'invio per l'acquisizione non invisibile all'utente. Nel gestore eventi eseguire il cast *di pValue* a un puntatore a una struttura [**WM GET LICENSE \_ \_ \_ DATA**](wm-get-license-data.md) ed esaminare il **membro hr** per determinare se la licenza è stata acquisita correttamente. Se **hr** è uguale a NS E DRM NO RIGHTS, indica che la licenza deve essere \_ acquisita in modo non \_ \_ \_ invisibile all'utente. Le applicazioni devono consentire agli utenti di annullare il processo di acquisizione delle licenze in qualsiasi momento. Questa operazione viene eseguita chiamando [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). La chiamata a questo metodo invierà un **evento WMT \_ ACQUIRE \_ LICENSE** con valore **HRESULT** pari a NS \_ S \_ DRM ACQUIRE \_ \_ CANCELLED.

Se **hr** è uguale a NS \_ S DRM LICENSE ACQUIRED, la licenza è stata acquisita e l'applicazione può tentare di riprodurre il file o copiarlo in un dispositivo o eseguire qualsiasi azione per cui ha richiesto i \_ \_ \_ diritti.

In Windows XP è stato introdotto un nuovo codice di errore: NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED. Questo codice di errore viene generato ogni volta che i componenti di run-time Windows Media Format in Windows XP non riescono ad acquisire una licenza durante l'acquisizione della licenza invisibile all'utente o non invisibile all'utente. In altre piattaforme, L'errore NS E DRM LICENSE STORE viene in genere restituito \_ \_ quando \_ \_ \_ l'acquisizione della licenza ha esito negativo. Il nuovo codice di errore è destinato a distinguere l'errore di acquisizione delle licenze da altre condizioni di errore in cui viene generato L'ERRORE DI ARCHIVIAZIONE LICENZE NS \_ E \_ \_ \_ \_ DRM.

Il modo consigliato per gestire questi errori quando vengono restituiti dopo un tentativo di acquisizione della licenza invisibile all'utente è illustrato nel frammento di codice seguente:


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> </dl>

 

 




