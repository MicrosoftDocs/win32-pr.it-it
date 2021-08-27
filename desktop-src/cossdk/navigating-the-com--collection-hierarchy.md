---
description: Esplorazione della gerarchia di raccolte COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Esplorazione della gerarchia di raccolte COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef6f23cd9f584b6cbe496fe7122abfa9978cd25cb28d81a5c89782b718138be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070451"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Esplorazione della gerarchia di raccolte COM+

Alcune raccolte che è possibile recuperare facilmente usando il [**metodo GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) nell'oggetto [**COMAdminCatalog.**](comadmincatalog.md) Questo metodo recupera una raccolta di "primo livello". ovvero una raccolta, ad esempio [**Applicazioni**](applications.md), che sta per se stessa e che è univoca e non sommata logicamente in un'altra raccolta.

Molte raccolte, tuttavia, vengono sommate logicamente in un'altra raccolta perché contengono elementi che fanno parte di una struttura più grande. Ad esempio, la raccolta [**Components**](components.md) viene sommata, o correlata, alla raccolta [**Applications**](applications.md) perché contiene i componenti installati in una particolare applicazione COM+, che a sua volta corrisponde a un elemento nella **raccolta Applications.** Le raccolte correlate come questa non sono univoche. è disponibile una **raccolta Components** per ogni applicazione distinta.

Di conseguenza, le raccolte vengono disposte in una struttura gerarchica che corrisponde naturalmente alle relazioni logiche tra gli elementi che contengono. Un diagramma della gerarchia di raccolta è disponibile in [Raccolte di amministrazione COM+.](com--administration-collections.md) Per molti degli elementi che si desidera configurare usando gli oggetti COMAdmin, è necessario spostarsi in una parte della gerarchia di raccolta per recuperare l'elemento appropriato.

Ciò significa in pratica che se si vuole ottenere un elemento in una raccolta correlata, è necessario eseguire tutte le operazioni necessarie di livello superiore, presupponendo prima le raccolte. Per recuperare una raccolta correlata, è necessario recuperare l'elemento specifico nella raccolta padre a cui è correlata la raccolta figlio. Ad esempio, se si vuole configurare un elemento corrispondente a un componente in una particolare applicazione COM+, è necessario eseguire la procedura seguente:

1.  Ottenere la [**raccolta**](applications.md) Applications e popolarla.
2.  Enumerare il contenuto della raccolta [**Applications**](applications.md) fino a ottenere l'elemento corrispondente all'applicazione COM+ corretta.
3.  Ottiene e popola la raccolta [**Components**](components.md) per quella particolare applicazione COM+.
4.  Enumerare il contenuto della raccolta [**Components**](components.md) fino a ottenere l'elemento corrispondente al componente corretto.

L'esempio Visual Basic Microsoft seguente illustra come eseguire i passaggi precedenti:


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



Nell'esempio precedente vengono usati due metodi **GetCollection** distinti. Il primo viene esposto [**da COMAdminCatalog**](comadmincatalog.md) e viene usato per ottenere una raccolta di primo livello, in questo caso "Applicazioni". Il secondo viene esposto da [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e viene usato per ottenere una raccolta correlata alla raccolta corrente. Si indica esattamente la raccolta desiderata passando il nome "Components" e il valore della proprietà Key dell'oggetto padre. Il valore della proprietà Key è spesso un nome o un GUID che identifica in modo univoco l'oggetto. Questo valore viene identificato nella documentazione per ogni raccolta.

Nel caso più generale, è necessario ottenere le raccolte correlate in modo iterativo verso il basso nella gerarchia di raccolte fino a quando non si recupera la raccolta desiderata. I passaggi da eseguire seguono lo stesso modello generale, in modo ripetitivo. Per un elenco completo delle raccolte, vedere [Raccolte di amministrazione COM+.](com--administration-collections.md)

In alcuni casi, è possibile usare un metodo di collegamento la seconda volta che si segue un percorso nella gerarchia di raccolta. È possibile usare questo metodo solo dopo aver già memorizzato nella cache tutti i valori key. Per informazioni dettagliate, [**vedere ICOMAdminCatalog::GetCollectionByQuery.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Popolamento di raccolte COM+](populating-com--collections.md)
</dt> <dt>

[Esecuzione di query per le raccolte correlate disponibili](querying-for-available-related-collections.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



