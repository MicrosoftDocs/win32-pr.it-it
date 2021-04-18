---
description: È possibile utilizzare lo strumento di amministrazione Servizi componenti per importare in applicazioni componenti specifici che sono già stati registrati nel computer come componenti COM nel registro di sistema di Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importazione di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483036"
---
# <a name="importing-components"></a>Importazione di componenti

È possibile utilizzare lo strumento di amministrazione Servizi componenti per importare in applicazioni componenti specifici che sono già stati registrati nel computer come componenti COM nel registro di sistema di Windows. L'importazione di un componente non comporta l'installazione delle informazioni sull'interfaccia o sul metodo necessarie per impostare le proprietà dell'interfaccia o per configurare l'accesso al componente da un client remoto. Pertanto, se possibile, è consigliabile installare anziché importare componenti non configurati.

> [!Note]  
> Quando si importa un componente in un'applicazione COM+, COM+ non popola le informazioni sul metodo e sull'interfaccia per il componente. Durante l'esportazione di un proxy di applicazione, COM+ non fornirà informazioni di marshalling (librerie dei tipi o proxy/stub) per alcune o tutte le interfacce. L'esportazione di proxy di applicazione contenenti componenti importati avrà esito negativo o verrà generato un avviso.

 

**Per importare un componente in un'applicazione COM+**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer che ospita l'applicazione COM+.

2.  Aprire la cartella **applicazioni com+** per il computer e selezionare l'applicazione in cui si desidera installare il componente.

3.  Aprire la cartella dell'applicazione e selezionare **componenti**.

4.  Scegliere **nuovo** dal menu **azione** , quindi fare clic su **componente**. È anche possibile fare clic con il pulsante destro del mouse sulla cartella **componenti** , scegliere **nuovo**, quindi fare clic su **componente**.

5.  Nella pagina **iniziale** dell'installazione guidata dell'applicazione com+, fare clic su **Avanti**, quindi nella finestra di dialogo **Importa o installa componente** fare clic su **Importa componente/i che sono già registrati**.

6.  Nella finestra di dialogo **scegliere i componenti da importare** , selezionare la casella di controllo **Dettagli** per visualizzare le informazioni complete sui componenti che sono già registrati. Selezionare i componenti che si desidera importare dall'elenco visualizzato, quindi fare clic su **Avanti**.

7.  Fare clic su **Fine**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Copia di componenti](copying-components.md)
</dt> <dt>

[Creazione di una nuova applicazione COM+](creating-a-new-com--application.md)
</dt> <dt>

[Eliminazione di un'applicazione COM+](deleting-a-com--application.md)
</dt> <dt>

[Installazione di nuovi componenti](installing-new-components.md)
</dt> <dt>

[Spostamento dei componenti](moving-components.md)
</dt> <dt>

[Rimozione di un componente da un'applicazione COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



