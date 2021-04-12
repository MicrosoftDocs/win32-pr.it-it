---
description: Le applicazioni utilizzano il buffer dello stencil per mascherare i pixel in un'immagine. La maschera controlla se il pixel viene disegnato o meno. Di seguito sono riportati alcuni degli effetti più comuni.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Tecniche di buffer di stencil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401340"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a>Tecniche di buffer di stencil (Direct3D 9)

Le applicazioni utilizzano il buffer dello stencil per mascherare i pixel in un'immagine. La maschera controlla se il pixel viene disegnato o meno. Di seguito sono riportati alcuni degli effetti più comuni.

-   [Composizione](compositing.md)
-   [Decaing](decaling.md)
-   [Dissolvenze, dissolvenze e scorrimenti](dissolves--fades--and-swipes.md)
-   [Strutture e sagome](outlines-and-silhouettes.md)
-   [Stencil a due lati](two-sided-stencil.md)

Il buffer dello stencil Abilita o Disabilita il disegno sulla superficie di destinazione del rendering in base a un pixel per pixel. Al livello più fondamentale, consente alle applicazioni di mascherare le sezioni dell'immagine di cui è stato eseguito il rendering in modo che non vengano visualizzate. Le applicazioni spesso utilizzano buffer di stencil per effetti speciali come dissolvenze, derivazione e struttura.

Le informazioni sul buffer dello stencil sono incorporate nei dati del buffer z. L'applicazione può usare il metodo [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) per verificare il supporto degli stencil hardware, come illustrato nell'esempio di codice seguente.


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) consente di scegliere un dispositivo da creare in base alle funzionalità del dispositivo. In questo caso, i dispositivi che non supportano i buffer di stencil a 8 bit vengono rifiutati. Si noti che questo è solo un possibile uso di **IDirect3D9:: CheckDeviceFormat**; per informazioni dettagliate, vedere [determinazione del supporto hardware (Direct3D 9)](determining-hardware-support.md).

## <a name="how-the-stencil-buffer-works"></a>Funzionamento del buffer dello stencil

Direct3D esegue un test sul contenuto del buffer dello stencil in base ai singoli pixel. Per ogni pixel nell'area di destinazione, viene eseguito un test utilizzando il valore corrispondente nel buffer dello stencil, un valore di riferimento dello stencil e un valore della maschera dello stencil. Se il test viene superato, Direct3D esegue un'azione. Il test viene eseguito seguendo questa procedura.

1.  Eseguire un'operazione con AND bit per bit del valore di riferimento dello stencil con la maschera dello stencil.
2.  Eseguire un'operazione con AND bit per bit del valore del buffer dello stencil per il pixel corrente con la maschera dello stencil.
3.  Confrontare il risultato del passaggio 1 con il risultato del passaggio 2, usando la funzione di confronto.

Questi passaggi sono illustrati nell'esempio di codice seguente.


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



contenuto del buffer dello stencil per il pixel corrente. Questo esempio di codice usa il simbolo e commerciale (&) per rappresentare l'operazione AND bit per bit.


```
StencilMask
```



rappresenta il valore della maschera di stencil e


```
StencilRef
```



rappresenta il valore di riferimento dello stencil.


```
CompFunc
```



è la funzione di confronto.

Il pixel corrente viene scritto nell'area di destinazione se il test di stencil viene superato e viene ignorato in caso contrario. Il comportamento di confronto predefinito consiste nel scrivere il pixel, indipendentemente dal modo in cui ogni operazione bit per bit viene disattivata (D3DCMP \_ sempre). È possibile modificare questo comportamento modificando il valore dello stato di \_ rendering STENCILFUNC di D3DRS, passando un membro del tipo enumerato [**D3DCMPFUNC**](./d3dcmpfunc.md) per identificare la funzione di confronto desiderata.

L'applicazione può personalizzare l'operazione del buffer dello stencil. Può impostare la funzione di confronto, la maschera dello stencil e il valore di riferimento dello stencil. È inoltre in grado di controllare l'azione eseguita da Direct3D quando il test di stencil ha esito positivo o negativo. Per ulteriori informazioni, vedere [lo stato del buffer dello stencil (Direct3D 9)](stencil-buffer-state.md).

## <a name="examples"></a>Esempio

Negli esempi di codice seguenti viene illustrata la configurazione del buffer dello stencil.


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



Per impostazione predefinita, il valore di riferimento dello stencil è zero. Qualsiasi valore integer è valido. Direct3D esegue un AND bit per bit del valore di riferimento dello stencil e un valore della maschera dello stencil prima del test dello stencil.

È possibile controllare le informazioni sui pixel scritte in base al confronto tra stencil.


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



È possibile scrivere una formula personalizzata per il valore che si desidera scrivere nel buffer dello stencil, come illustrato nell'esempio seguente.


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline pixel](pixel-pipeline.md)
</dt> </dl>

 

 
