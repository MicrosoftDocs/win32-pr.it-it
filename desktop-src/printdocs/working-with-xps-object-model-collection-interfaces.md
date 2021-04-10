---
description: Viene descritto come utilizzare i metodi comuni delle interfacce di raccolta.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Uso delle interfacce di raccolta OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232134"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Uso delle interfacce di raccolta OM XPS

Viene descritto come utilizzare i metodi comuni delle interfacce di raccolta.

## <a name="contents"></a>Contenuto

I metodi descritti in questa sezione sono illustrati nell'elenco seguente. Non tutte le interfacce di raccolta supportano ognuno di questi metodi e alcune interfacce supportano anche metodi non descritti in questa pagina. Per l'elenco dei metodi supportati da un'interfaccia specifica, fare riferimento alla descrizione della descrizione di tale interfaccia.

<dl>

[Append (metodo)](#append-method)  
[Metodo GetAt](#getat-method)  
[Metodo GetCount](#getcount-method)  
[Metodo InsertAt](#insertat-method)  
[RemoveAt (metodo)](#removeat-method)  
[Metodo SetAt](#setat-method)  
</dl>

[Vedere anche](#see-also)

## <a name="append-method"></a>Append (metodo)

Accoda un oggetto alla fine della raccolta.

**Sintassi generica**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**Descrizione**

Alla fine della raccolta, questo metodo aggiunge un oggetto che viene passato nell'elenco di parametri, come illustrato nel diagramma seguente.

![figura che Mostra come accodare aggiunge una voce alla raccolta](images/generic-append.png)

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

Scrive l'oggetto archiviato nel percorso della raccolta specificato dall' *Indice* nella variabile a cui fa riferimento l' *oggetto*. Questa azione non modifica il contenuto della raccolta. La figura seguente illustra questo processo.

![una figura che Mostra come il metodo Geta recupera una voce dalla raccolta](images/generic-getat.png)

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

![figura che mostra il modo in cui GetCount ottiene il numero di voci nella raccolta](images/generic-getcount.png)

## <a name="insertat-method"></a>Metodo InsertAt

Inserisce un oggetto in una posizione specificata della raccolta.

**Sintassi generica**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descrizione**

L'oggetto passato nell' *oggetto* viene inserito nella raccolta in corrispondenza della posizione specificata da *index*. Prima di inserire il nuovo *oggetto*, questo metodo viene spostato di 1 nell'oggetto che in precedenza occupava la posizione in corrispondenza dell' *Indice* e sposta tutti i puntatori di interfaccia successivi a *index*. La figura seguente illustra questo processo.

![figura che Mostra come InsertAt aggiunge una voce alla raccolta](images/generic-insertat.png)

## <a name="removeat-method"></a>RemoveAt (metodo)

Rimuove l'oggetto da una posizione specificata nella raccolta.

**Sintassi generica**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Descrizione**

Questo metodo rilascia l'oggetto dalla posizione specificata da *index*, quindi compatta la raccolta riducendo di 1 l'indice di ogni puntatore successivo a *index*. La figura seguente illustra questo processo.

![figura che illustra in che modo RemoveAt rimuove una voce dalla raccolta](images/generic-removeat.png)

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

Questo metodo prima rilascia l'oggetto in corrispondenza della posizione a cui fa riferimento *index*, quindi sostituisce tale oggetto con quello passato all' *oggetto*. La figura seguente illustra questo processo.

![figura che Mostra come SetAt sostituisce una voce nella raccolta](images/generic-setat.png)

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

 

 



