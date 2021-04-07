---
description: Per aggiungere componenti alla cartella componenti di un'applicazione COM+, è possibile utilizzare la procedura guidata di installazione dei componenti COM+ o trascinare i file dll che contengono i componenti da Esplora risorse e rilasciarli nell'applicazione.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installazione di nuovi componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049224"
---
# <a name="installing-new-components"></a>Installazione di nuovi componenti

Per aggiungere componenti alla cartella **componenti** di un'applicazione com+, è possibile utilizzare la procedura guidata di installazione dei componenti com+ o trascinare i file dll che contengono i componenti da Esplora risorse e rilasciarli nell'applicazione.

Se si utilizza l'installazione guidata componenti COM+, è possibile installare un nuovo componente che registra il componente nel computer oppure importa i componenti che sono già stati registrati. I componenti possono essere aggiunti a applicazioni vuote o a applicazioni esistenti.

**Per aggiungere un componente a un'applicazione COM+**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer che ospita l'applicazione COM+.

2.  Aprire la cartella **applicazioni com+** per il computer e selezionare l'applicazione in cui si desidera installare i componenti.

3.  Aprire la cartella dell'applicazione e selezionare **componenti**.

4.  Scegliere **nuovo** dal menu **azione** , quindi fare clic su **componente**. È anche possibile fare clic con il pulsante destro del mouse sulla cartella **componenti** , scegliere **nuovo**, quindi fare clic su **componente**.

5.  Nella pagina **iniziale** dell'installazione guidata dell'applicazione com+, fare clic su **Avanti**, quindi nella finestra di dialogo **Importa o installa componente** fare clic su **Installa nuovi componenti** .

6.  Nella finestra di dialogo **Installa nuovi componenti** fare clic su **Aggiungi** per cercare il componente che si desidera aggiungere.

7.  Nella finestra di dialogo **selezionare i file da installare** Digitare il nome del file del componente da installare o selezionare un nome di file nell'elenco visualizzato. Fare clic su **Apri**.

    Dopo aver aggiunto i file, nella finestra di dialogo **Installa nuovi componenti** verranno visualizzati i file aggiunti e i componenti associati. Se si seleziona la casella di controllo **Dettagli** , vengono visualizzate ulteriori informazioni sul contenuto dei file e sui componenti trovati.

    > [!Note]  
    > I componenti COM non configurati devono avere una libreria dei tipi. Se COM+ non riesce a trovare la libreria dei tipi del componente, il componente non verrà visualizzato nell'elenco. È anche possibile rimuovere un file dall'elenco **file da installare** selezionandolo e facendo clic su **Rimuovi**.

     

8.  Fare clic su **Avanti** e quindi su **fine** per installare il componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Copia di componenti](copying-components.md)
</dt> <dt>

[Creazione di una nuova applicazione COM+](creating-a-new-com--application.md)
</dt> <dt>

[Eliminazione di un'applicazione COM+](deleting-a-com--application.md)
</dt> <dt>

[Importazione di componenti](importing-components.md)
</dt> <dt>

[Spostamento dei componenti](moving-components.md)
</dt> <dt>

[Rimozione di un componente da un'applicazione COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



