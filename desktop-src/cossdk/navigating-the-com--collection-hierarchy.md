---
description: Esplorazione della gerarchia della raccolta COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Esplorazione della gerarchia della raccolta COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304816"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Esplorazione della gerarchia della raccolta COM+

Alcune raccolte che è possibile recuperare facilmente usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) nell'oggetto [**COMAdminCatalog**](comadmincatalog.md) . Questo metodo recupera una raccolta "di primo livello"; ovvero una raccolta, ad esempio [**applicazioni**](applications.md), che si basa su se stessa e che è univoca e non è inglobata logicamente in un'altra raccolta.

Molte raccolte, tuttavia, sono inglobate logicamente in un'altra raccolta perché contengono elementi che fanno parte di una struttura più grande. La raccolta [**Components**](components.md) , ad esempio, è inglobata o correlata alla raccolta di [**applicazioni**](applications.md) perché contiene i componenti installati in una particolare applicazione com+, che a sua volta corrisponde a un elemento nella raccolta di **applicazioni** . Le raccolte correlate, ad esempio, non sono univoche. è disponibile una raccolta di **componenti** per ogni applicazione distinta.

Pertanto, le raccolte sono disposte in una struttura gerarchica che corrisponde naturalmente alle relazioni logiche tra gli elementi in essi contenuti. Un diagramma della gerarchia della raccolta è reperibile in [raccolte di amministrazione com+](com--administration-collections.md). Per molti degli elementi che si desidera configurare utilizzando gli oggetti COMAdmin, è necessario spostarsi in una parte della gerarchia della raccolta per recuperare l'elemento appropriato.

Ciò significa che se si vuole ottenere un elemento in una raccolta correlata, è necessario eseguire prima di tutto il livello superiore necessario, ovvero le raccolte classificato. Per recuperare una raccolta correlata, è necessario recuperare l'elemento specifico nella raccolta padre a cui è correlata la raccolta figlio. Se, ad esempio, si desidera configurare un elemento corrispondente a un componente in una particolare applicazione COM+, è necessario eseguire i passaggi seguenti:

1.  Ottenere la raccolta di [**applicazioni**](applications.md) e compilarla.
2.  Consente di enumerare il contenuto della raccolta di [**applicazioni**](applications.md) fino a quando non si ottiene l'elemento corrispondente all'applicazione COM+ corretta.
3.  Ottenere e popolare la raccolta di [**componenti**](components.md) per quella particolare applicazione com+.
4.  Enumerare il contenuto della raccolta [**Components**](components.md) fino a quando non si ottiene l'elemento corrispondente al componente corretto.

Nell'esempio di Visual Basic Microsoft riportato di seguito viene illustrato come eseguire i passaggi precedenti:


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



Nell'esempio precedente vengono usati due metodi **GetCollection** distinti. Il primo è esposto da [**COMAdminCatalog**](comadmincatalog.md) e viene usato per ottenere una raccolta di primo livello, in questo caso "Applications". Il secondo è esposto da [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e viene usato per ottenere una raccolta correlata alla raccolta corrente. è possibile indicare con precisione la raccolta desiderata passando il nome "Components" e il valore della proprietà chiave dell'oggetto padre. Il valore della proprietà Key è spesso un nome o un GUID che identifica in modo univoco l'oggetto; Questo valore viene identificato nella documentazione per ogni raccolta.

Nel caso più generale, è necessario ottenere le raccolte correlate in modo iterativo nella gerarchia della raccolta fino a quando non si recupera la raccolta desiderata. La procedura da seguire è la stessa del modello generale, ripetutamente. Per un elenco completo delle raccolte, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).

In alcuni casi, potrebbe essere necessario usare un metodo di collegamento la seconda volta che si segue un percorso attraverso la gerarchia di raccolta. È possibile utilizzare questo metodo solo dopo aver già memorizzato nella cache tutti i valori di chiave che interessano. Per informazioni dettagliate, vedere [**ICOMAdminCatalog:: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Popolamento di raccolte COM+](populating-com--collections.md)
</dt> <dt>

[Esecuzione di query per le raccolte correlate disponibili](querying-for-available-related-collections.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



