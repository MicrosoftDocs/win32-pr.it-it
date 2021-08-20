---
description: Viene descritto come usare i metodi comuni delle interfacce di raccolta.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Uso delle interfacce di raccolta OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a23e9c217f84c1baf5b0cf846f706098da34f4f32ad2e90cd2c13392d9019164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685640"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Uso delle interfacce di raccolta OM XPS

Viene descritto come usare i metodi comuni delle interfacce di raccolta.

## <a name="contents"></a>Contenuto

I metodi descritti in questa sezione sono illustrati nell'elenco seguente. Non tutte le interfacce di raccolta supportano ognuno di questi metodi e alcune interfacce supportano anche i metodi non descritti in questa pagina. Per l'elenco dei metodi supportati da un'interfaccia specifica, fare riferimento alla descrizione dell'interfaccia.

<dl>

[Metodo Append](#append-method)  
[Metodo GetAt](#getat-method)  
[Metodo GetCount](#getcount-method)  
[Metodo InsertAt](#insertat-method)  
[Metodo RemoveAt](#removeat-method)  
[Metodo SetAt](#setat-method)  
</dl>

[Vedere anche](#see-also)

## <a name="append-method"></a>Metodo Append

Aggiunge un oggetto alla fine dell'insieme.

**Sintassi generica**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**Descrizione**

Alla fine della raccolta, questo metodo aggiunge un oggetto passato nell'elenco di parametri, come illustrato nel diagramma seguente.

![figura che mostra come append aggiunge una voce alla raccolta](images/generic-append.png)

## <a name="getat-method"></a>Metodo GetAt

Ottiene un oggetto da una posizione specificata nella raccolta.

**Sintassi generica**


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



**Descrizione**

Scrive l'oggetto archiviato nella posizione della raccolta specificata *dall'indice* nella variabile a cui fa riferimento *l'oggetto*. Questa azione non modifica il contenuto della raccolta. La figura seguente illustra questo processo.

![figura che mostra come getat recupera una voce dalla raccolta](images/generic-getat.png)

## <a name="getcount-method"></a>Metodo GetCount

Ottiene il numero di oggetti archiviati nella raccolta.

**Sintassi generica**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**Descrizione**

Scrive il numero di oggetti attualmente archiviati nella raccolta nella variabile a cui fa riferimento *count*. Questa azione non modifica il contenuto della raccolta. La figura seguente illustra questo processo.

![figura che mostra come getcount ottiene il numero di voci nella raccolta](images/generic-getcount.png)

## <a name="insertat-method"></a>Metodo InsertAt

Inserisce un oggetto in una posizione specificata dell'insieme.

**Sintassi generica**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descrizione**

L'oggetto passato *nell'oggetto* viene inserito nella raccolta in corrispondenza della posizione specificata *dall'indice*. Prima di inserire il *nuovo* oggetto , questo metodo sposta di  1 l'oggetto che in precedenza occupava la posizione in corrispondenza dell'indice e sposta tutti i puntatori a interfaccia successivi *all'indice*. La figura seguente illustra questo processo.

![figura che illustra come insertat aggiunge una voce alla raccolta](images/generic-insertat.png)

## <a name="removeat-method"></a>Metodo RemoveAt

Rimuove l'oggetto da una posizione specificata nella raccolta.

**Sintassi generica**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Descrizione**

Questo metodo rilascia l'oggetto dalla posizione specificata dall'indice *,* quindi compatta la raccolta riducendo di 1 l'indice di ogni puntatore successivo *all'indice*. La figura seguente illustra questo processo.

![figura che mostra come removeat rimuove una voce dalla raccolta](images/generic-removeat.png)

## <a name="setat-method"></a>Metodo SetAt

Sostituisce l'oggetto in una posizione specificata nella raccolta.

**Sintassi generica**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descrizione**

Questo metodo rilascia prima l'oggetto nella posizione a cui fa riferimento l'indice *,* quindi sostituisce l'oggetto con quello passato *nell'oggetto*. La figura seguente illustra questo processo.

![figura che mostra come setat sostituisce una voce nella raccolta](images/generic-setat.png)

## <a name="see-also"></a>Vedere anche

<dl>

[**IXpsOMColorProfileResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[**IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[**IXpsOMFontResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[**IXpsOMGeometryFigureCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[**IXpsOMGradientStopCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[**IXpsOMImageResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[**IXpsOMSignatureBlockResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



