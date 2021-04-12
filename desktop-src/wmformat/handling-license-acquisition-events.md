---
title: Gestione degli eventi di acquisizione delle licenze
description: Gestione degli eventi di acquisizione delle licenze
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media Format SDK, gestione degli eventi di acquisizione delle licenze
- Windows Media Format SDK, eventi di acquisizione della licenza
- Formato di sistemi avanzati (ASF), gestione degli eventi di acquisizione delle licenze
- ASF (Advanced Systems Format), gestione degli eventi di acquisizione delle licenze
- ASF (Advanced Systems Format), eventi di acquisizione della licenza
- ASF (formato avanzato dei sistemi), eventi di acquisizione della licenza
- Digital Rights Management (DRM), gestione degli eventi di acquisizione delle licenze
- DRM (Digital Rights Management), gestione degli eventi di acquisizione delle licenze
- Digital Rights Management (DRM), eventi di acquisizione della licenza
- DRM (Digital Rights Management), eventi di acquisizione della licenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398588"
---
# <a name="handling-license-acquisition-events"></a>Gestione degli eventi di acquisizione delle licenze

Un'applicazione Reader abilitata per DRM, nel metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback, gestisce i quattro eventi seguenti relativi al processo di acquisizione della licenza:

-   **\_stato della \_ firma \_ LICENSEURL di WMT**
-   **\_nessun \_ diritto di WMT**
-   **WMT \_ No \_ Rights \_**
-   **\_licenza di acquisizione WMT \_**

**\_stato della \_ firma \_ LICENSEURL di WMT**

Quando il componente DRM rileva il contenuto protetto da DRM versione 7, cerca innanzitutto una licenza valida nel sistema locale. Se non ne esiste alcuno, viene valutato l'URL di acquisizione della licenza nell'intestazione DRM del file e viene inviato un evento **\_ \_ \_ dello stato della firma WMT LICENSEURL** con *pValue* impostato su uno dei valori di [**\_ \_ attendibilità di WMT DRMLA**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , che indica se l'URL è attendibile, non attendibile o è stato manomesso. Se l'URL non è attendibile, l'applicazione deve avvisare l'utente. Se l'URL è stato manomesso, il file deve essere considerato danneggiato e l'applicazione non deve passare all'URL senza emettere un avviso sicuro per l'utente.

**\_nessun \_ diritto di WMT**

L'evento **WMT \_ No \_ Rights** viene inviato solo per il contenuto DRM versione 1, il che significa che la licenza deve essere acquisita in modo non invisibile. In altre parole, l'utente deve passare a una pagina Web per acquisire una licenza. L'URL della pagina viene recuperato come stringa a caratteri wide con terminazione null dal parametro *pValue* nel metodo **OnStatus** .

Se appropriato, un'applicazione può semplificare l'esplorazione della pagina Web da parte dell'utente, aprendo Internet Explorer in un processo separato oppure ospitando il controllo Web browser. Questa operazione non è tuttavia necessaria. Come minimo, un'applicazione può semplicemente visualizzare l'URL dell'utente in una finestra di messaggio e richiedere di incollarlo nella barra degli indirizzi di Internet Explorer. Nell'esempio AudioPlayer viene illustrata la gestione corretta dell'evento **WMT \_ No \_ Rights** , tra cui come formattare la stringa URL e come utilizzare il metodo **CreateProcess** per aprire Internet Explorer e passare all'URL specificato.

Poiché l'applicazione non è in grado di sapere quando è stata acquistata una licenza di DRM versione 1, spetta all'utente tentare di aprire nuovamente il file dopo l'acquisizione della licenza.

Questo stesso processo di acquisizione della licenza non invisibile all'utente può essere usato anche per le licenze della versione 7, ma in questo caso l'applicazione può chiamare prima [**IWMDRMReader:: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition). Questo metodo provocherà ripetutamente il controllo dell'archivio licenze locale fino a quando non viene trovata la licenza per il nuovo file. A questo punto, l'applicazione riceverà un evento **WMT \_ acquire \_ License** . Per tutte le licenze della versione 7, è consigliabile che le applicazioni forniscano agli utenti la possibilità di ottenere le licenze in modo invisibile o non invisibile all'utente.

**WMT \_ No \_ Rights \_**

Il **WMT \_ No \_ Rights \_ ex** evento indica che il contenuto è protetto da DRM versione 7 e pertanto il processo di acquisizione della licenza può procedere in modo invisibile all'utente o non automatico. In generale, l'acquisizione di licenze Silent è più utile per gli utenti finali, anche se alcune persone preferiscono acquisire tutte le licenze in modo non invisibile. Quando l'acquisizione della licenza richiede che l'utente invii informazioni di pagamento o personali, il processo deve sempre essere eseguito in modo non invisibile. L'acquisizione della licenza non invisibile all'utente è descritta in precedenza sotto l'intestazione **WMT \_ No \_ Rights** . L'acquisizione invisibile all'utente procede come segue:

1.  Eseguire il cast del parametro *pValue* a una struttura di [**dati di \_ \_ licenza \_ WM Get**](wm-get-license-data.md) e archiviare la struttura nel caso in cui sia necessaria in un secondo momento per l'acquisizione della licenza non invisibile all'utente.
2.  Chiamare **QueryInterface** sull'oggetto Reader per ottenere l'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
3.  Chiamare [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) e specificare 0x1 nel parametro *dwFlags* per indicare l'acquisizione della lingua invisibile all'utente. Si tratta di una chiamata asincrona che restituisce immediatamente un risultato.
4.  Attendere l'evento **WMT \_ acquire \_ License** .

**\_licenza di acquisizione WMT \_**

L'evento **WMT \_ acquisisce \_ License** viene inviato al termine del processo di acquisizione della licenza per una licenza DRM versione 7. [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) fa sì che questo evento venga inviato per l'acquisizione invisibile all'utente e [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) ne causa l'invio per l'acquisizione non invisibile all'utente. Nel gestore eventi, eseguire il cast di *pValue* a un puntatore a una struttura di [**dati di \_ \_ licenza \_ WM Get**](wm-get-license-data.md) ed esaminare il membro **HR** per determinare se la licenza è stata acquisita correttamente. Se **HR** è uguale a NS \_ E \_ DRM \_ No \_ Rights, indica che la licenza deve essere acquisita in modo non invisibile. Le applicazioni devono consentire agli utenti di annullare il processo di acquisizione delle licenze in qualsiasi momento. Questa operazione viene eseguita chiamando [**IWMDRMReader:: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). La chiamata a questo metodo invierà un evento **WMT \_ acquire \_ License** con un valore **HRESULT** di NS \_ S \_ DRM \_ acquire \_ annullato.

Se **HR** corrisponde alla \_ licenza DRM di NS S \_ \_ \_ acquistata, la licenza è stata acquisita e l'applicazione può provare a riprodurre il file oppure copiarla in un dispositivo o eseguire qualsiasi azione per cui aveva richiesto diritti.

In Windows XP è stato introdotto un nuovo codice di errore: NS \_ E \_ DRM \_ License \_ NOTACQUIRED. Questo codice di errore viene generato ogni volta che i componenti di runtime di Windows Media Format in Windows XP non riescono ad acquisire una licenza durante l'acquisizione di una licenza invisibile all'utente o non interattiva. In altre piattaforme, l' \_ \_ errore dell'archivio licenze NS E DRM viene in \_ \_ \_ genere restituito quando l'acquisizione della licenza ha esito negativo. Il nuovo codice di errore è destinato a distinguere gli errori di acquisizione della licenza da altre condizioni di errore in cui \_ \_ \_ viene generato l'errore dell'archivio licenze NS E DRM \_ \_ .

Il metodo consigliato per gestire questi errori quando vengono restituiti dopo che è stato eseguito un tentativo di acquisizione di una licenza invisibile all'utente nel seguente frammento di codice:


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
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> </dl>

 

 




