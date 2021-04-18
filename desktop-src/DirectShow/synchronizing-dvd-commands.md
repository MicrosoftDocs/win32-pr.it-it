---
description: Sincronizzazione dei comandi DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Sincronizzazione dei comandi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318352"
---
# <a name="synchronizing-dvd-commands"></a>Sincronizzazione dei comandi DVD

I comandi DVD non vengono sempre completati immediatamente. Per questo motivo, alcuni dei metodi in [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sono asincroni. Sono inclusi i metodi di riproduzione, ad esempio **PlayTitle**, e i metodi di navigazione dei menu, ad esempio **ShowMenu** e **ReturnFromSubmenu**. Un metodo asincrono restituisce immediatamente un risultato, senza attendere il completamento del comando. Dopo la restituzione del metodo, altri eventi possono impedire il completamento del comando, anche se il metodo ha avuto esito positivo. DirectShow offre diverse opzioni per la sincronizzazione dei comandi, che vanno da nessuna sincronizzazione alla sincronizzazione completa usando gli eventi del grafo del filtro.

Tutti i metodi asincroni hanno un parametro *dwFlags* e un parametro *ppCmd* . Il parametro *dwFlags* specifica il comportamento di sincronizzazione e il parametro *ppCmd* restituisce un puntatore a un oggetto di sincronizzazione facoltativo. Comportamenti diversi variano a seconda dei valori specificati per questi parametri.

**Nessuna sincronizzazione**

Per un'applicazione di riproduzione DVD di base, l'opzione migliore potrebbe essere semplicemente ignorare i problemi di sincronizzazione. Occasionalmente, un comando può avere esito negativo o l'interfaccia utente potrebbe essere leggermente in ritardo durante l'aggiornamento, ma questi errori saranno in ordine di frazioni di secondi.

Per eseguire un comando senza sincronizzazione, impostare il flag del flag di comando DVD \_ \_ \_ None nel parametro *dwFlags* e impostare il parametro *ppCmd* su **null**:


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Processi bloccati**

Se si imposta il \_ \_ flag di blocco del flag CMD del DVD EC \_ \_ nel parametro *dwFlags* , il metodo si blocca fino al completamento del comando:


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



In effetti, questo flag converte un metodo asincrono in un metodo sincrono. Lo svantaggio è che l'interfaccia utente si blocca se si chiama il metodo dal thread dell'applicazione.

**Oggetto di sincronizzazione**

Tutti i metodi asincroni possono restituire un oggetto di sincronizzazione, che può essere usato per attendere l'avvio o la fine del comando. Per ottenere questo oggetto, passare l'indirizzo di un puntatore [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) nel parametro *ppCmd* :


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Se il metodo ha esito positivo, restituisce un nuovo oggetto **IDvdCmd** . Il metodo [**IDvdCmd:: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) si blocca fino all'inizio del comando e il metodo [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) si blocca fino alla fine del comando. Il valore restituito indica lo stato del comando.

Dal punto di vista funzionale, il codice seguente equivale all'impostazione del \_ flag di blocco del flag CMD del DVD EC \_ \_ \_ , illustrato in precedenza.


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



In questo caso, il metodo **PlayTitle** non viene bloccato, ma l'applicazione viene bloccata chiamando **WaitForEnd**.

**Eventi dello stato del comando**

Se si imposta il flag SendEvents del DVD del \_ \_ flag CMD \_ nel parametro *dwFlags* , il navigatore DVD invia un evento di [**\_ \_ \_ avvio cmd del DVD EC**](ec-dvd-cmd-start.md) quando il comando inizia e un evento di [**\_ \_ \_ fine del cmd DVD EC**](ec-dvd-cmd-end.md) quando il comando termina.

Il parametro *lParam2* dell'evento è il valore restituito HRESULT per il comando. Il parametro *lParam1* dell'evento fornisce un modo per ottenere l'oggetto di sincronizzazione per il comando. Se si passa *lParam1* al metodo [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , il metodo restituisce un puntatore all'interfaccia **IDvdCmd** dell'oggetto di sincronizzazione. È possibile usare questa interfaccia per attendere il completamento del comando, come descritto in precedenza. Tuttavia, se è stato passato **null** per il parametro *PpCmd* nel metodo **IDVDControl2** originale, il navigatore DVD non creerà un oggetto di sincronizzazione e **GetCmdFromEvent** restituirà e \_ avrà esito negativo.

Nel codice seguente viene illustrato come utilizzare gli eventi di stato del comando senza alcun oggetto di sincronizzazione.


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



Si noti che senza un oggetto di sincronizzazione, non è possibile stabilire quale comando è associato all'evento. Nel codice seguente viene illustrato come utilizzare gli eventi con l'oggetto di sincronizzazione. L'idea è archiviare gli oggetti di sincronizzazione in un elenco e quindi confrontare i puntatori a oggetti quando si ottiene l'evento di [**\_ \_ \_ inizio**](ec-dvd-cmd-start.md) del cmd di DVD EC o del [**\_ \_ cmd \_**](ec-dvd-cmd-end.md) .


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



**Scaricamento dei buffer di DVD Navigator**

Durante la riproduzione, il navigatore DVD memorizza nel buffer i dati video. La quantità di dati memorizzati nel buffer varia. Quando lo strumento di spostamento DVD passa a una nuova parte di video, i dati già presenti nella pipeline non vengono persi, quindi la transizione è trasparente. Per impostazione predefinita, quando il navigatore DVD emette un comando, non Scarica i dati già presenti nella pipeline. Di conseguenza, potrebbe verificarsi una certa latenza prima che sia possibile visualizzare l'effetto del comando, a seconda della quantità di dati memorizzati nel buffer. Per aumentare la velocità di risposta, è possibile forzare lo scaricamento del navigatore DVD impostando il \_ \_ flag di scaricamento del flag di comando DVD \_ .


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Questo flag può essere combinato con uno qualsiasi dei flag descritti in precedenza, usando un operatore OR bit per bit. Un effetto collaterale dello scaricamento è che è possibile che alcuni video vadano persi, quindi non usare questo flag se è necessario garantire che non vi siano gap nel video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



