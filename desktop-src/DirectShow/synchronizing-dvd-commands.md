---
description: Sincronizzazione dei comandi DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Sincronizzazione dei comandi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38696425892618f1b66544e69a4a567d0f539234d991cb96792eda4f6f1509d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964811"
---
# <a name="synchronizing-dvd-commands"></a>Sincronizzazione dei comandi DVD

I comandi DVD non vengono sempre completati immediatamente. Per questo motivo, alcuni dei metodi in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sono asincroni. Sono inclusi i metodi di riproduzione, ad **esempio PlayTitle,** e i metodi di navigazione dei menu, ad esempio **ShowMenu** **e ReturnFromSubmenu.** Un metodo asincrono viene restituito immediatamente, senza attendere il completamento del comando. Dopo la fine del metodo, altri eventi possono impedire il completamento del comando, anche se il metodo ha avuto esito positivo. DirectShow offre diverse opzioni per la sincronizzazione dei comandi, dall'assenza di sincronizzazione alla sincronizzazione completa tramite gli eventi del grafico dei filtri.

Tutti i metodi asincroni hanno un *parametro dwFlags* e un *parametro ppCmd.* Il *dwFlags parametro specifica* il comportamento di sincronizzazione e il *ppCmd* parametro restituisce un puntatore a un oggetto di sincronizzazione facoltativo. Si verificano comportamenti diversi a seconda dei valori forniti per questi parametri.

**Nessuna sincronizzazione**

Per un'applicazione di riproduzione DVD di base, l'opzione migliore può essere semplicemente ignorare i problemi di sincronizzazione. In alcuni casi un comando potrebbe non riuscire o l'interfaccia utente potrebbe essere leggermente in ritardo durante l'aggiornamento, ma questi errori saranno nell'ordine di frazioni di secondi.

Per eseguire un comando senza sincronizzazione, impostare il flag DVD CMD FLAG Nessuno nel \_ \_ parametro \_ *dwFlags* e impostare il *parametro ppCmd* su **NULL:**


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Processi bloccati**

Se si imposta il flag EC DVD CMD FLAG Block nel \_ \_ parametro \_ \_ *dwFlags,* il metodo si blocca fino al completamento del comando:


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



In effetti, questo flag trasforma un metodo asincrono in un metodo sincrono. Lo svantaggio è che l'interfaccia utente si blocca se si chiama il metodo dal thread dell'applicazione.

**Oggetto di sincronizzazione**

Tutti i metodi asincroni possono restituire un oggetto di sincronizzazione, che è possibile usare per attendere l'avvio o la fine del comando. Per ottenere questo oggetto, passare l'indirizzo di un [**puntatore IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) nel *parametro ppCmd:*


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Se il metodo ha esito positivo, restituisce un nuovo **oggetto IDvdCmd.** Il [**metodo IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) si blocca fino all'inizio del comando e il metodo [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) si blocca fino al termine del comando. Il valore restituito indica lo stato del comando.

Dal punto di vista funzionale, il codice seguente equivale all'impostazione del flag EC \_ DVD \_ CMD FLAG \_ \_ Block, illustrato in precedenza.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



In questo caso, il **metodo PlayTitle** non si blocca, ma l'applicazione si blocca chiamando **WaitForEnd.**

**Eventi di stato dei comandi**

Se si imposta il flag Dvd \_ CMD FLAG SendEvents nel parametro \_ \_ *dwFlags,* [**\_ \_ \_**](ec-dvd-cmd-end.md) [**\_ \_ \_**](ec-dvd-cmd-start.md) lo strumento di navigazione DVD invia un evento EC DVD CMD START all'inizio del comando e un evento EC DVD CMD END al termine del comando.

Il parametro *lParam2 dell'evento* è il valore restituito HRESULT per il comando. Il parametro *lParam1 dell'evento* consente di ottenere l'oggetto di sincronizzazione per il comando. Se si passa *lParam1* al metodo [**IDvdInfo2::GetCmdFromEvent,**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) il metodo restituisce un puntatore all'interfaccia **IDvdCmd** dell'oggetto di sincronizzazione. È possibile usare questa interfaccia per attendere il completamento del comando, come descritto in precedenza. Tuttavia, se è stato passato **NULL** per il *parametro ppCmd* nel metodo **IDvdControl2** originale, dvd Navigator non crea un oggetto di sincronizzazione e **GetCmdFromEvent** restituisce E \_ FAIL.

Nel codice seguente viene illustrato come utilizzare gli eventi di stato dei comandi senza alcun oggetto di sincronizzazione.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



Si noti che senza un oggetto di sincronizzazione, non è possibile indicare quale comando è associato all'evento. Nel codice seguente viene illustrato come utilizzare gli eventi con l'oggetto di sincronizzazione. L'idea è archiviare gli oggetti di sincronizzazione in un elenco e quindi confrontare i puntatori agli oggetti quando si ottiene l'evento [**EC \_ DVD CMD \_ \_ START**](ec-dvd-cmd-start.md) o [**EC DVD CMD \_ \_ \_ END.**](ec-dvd-cmd-end.md)


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



**Scaricamento dei buffer dello strumento di navigazione DVD**

Durante la riproduzione, lo strumento di navigazione DVD bufferi i dati video. La quantità di dati memorizzati nel buffer varia. Quando lo strumento di navigazione DVD passa a un nuovo video, i dati già presenti nella pipeline non vengono persi, quindi la transizione è senza problemi. Per impostazione predefinita, quando lo strumento di navigazione DVD esegue un comando, non scarica i dati già nella pipeline. Di conseguenza, potrebbe esserci una certa latenza prima di poter vedere l'effetto del comando, a seconda della quantità di dati memorizzati nel buffer. Per aumentare la velocità di risposta, è possibile forzare lo scaricamento dello strumento di spostamento DVD impostando il flag DI SCARICAMENTO DEL DVD \_ CMD \_ \_ FLAG.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Questo flag può essere combinato con uno qualsiasi dei flag descritti in precedenza, usando un OR bit per bit. Un effetto collaterale dello scaricamento è che alcuni video potrebbero andare persi, quindi non usare questo flag se è necessario garantire che non ci siano gap nel video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



