---
description: Per aggiungere componenti alla cartella Componenti di un'applicazione COM+, è possibile usare l'Installazione guidata componenti COM+ oppure trascinare i file .dll che contengono i componenti da Esplora Windows e rilasciarli nell'applicazione.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installazione di nuovi componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af51bf28ce93e2d68dd1a07609c48c506911310781e8c5a0573017d43e022353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813591"
---
# <a name="installing-new-components"></a>Installazione di nuovi componenti

Per aggiungere componenti alla cartella **Componenti** di un'applicazione COM+, è possibile usare l'Installazione guidata componenti COM+ oppure trascinare i file .dll che contengono i componenti da Esplora Windows e rilasciarli nell'applicazione.

Se si usa l'Installazione guidata componenti COM+, è possibile installare un nuovo componente, che registra il componente nel computer, oppure importare componenti già registrati. È possibile aggiungere componenti ad applicazioni vuote o ad applicazioni esistenti.

**Per aggiungere un componente a un'applicazione COM+**

1.  Nell'albero della console dello strumento amministrativo Servizi componenti selezionare il computer che ospita l'applicazione COM+.

2.  Aprire la **cartella Applicazioni COM+** per il computer e selezionare l'applicazione in cui si desidera installare i componenti.

3.  Aprire la cartella dell'applicazione e selezionare **Componenti**.

4.  Scegliere **Nuovo** dal menu Azione **e** quindi fare clic su **Componente**. È anche possibile fare clic con il pulsante destro **del mouse sulla cartella Componenti** , scegliere **Nuovo** e quindi fare clic su **Componente**.

5.  Nella pagina **iniziale** dell'Installazione guidata applicazione COM+ fare  clic su Avanti **e** quindi nella finestra di dialogo Importa o installa un componente fare clic su Installa **nuovi componenti** .

6.  Nella finestra **di dialogo Installa nuovi** componenti fare clic su **Aggiungi** per cercare il componente da aggiungere.

7.  Nella finestra **di dialogo Seleziona file** da installare digitare il nome file del componente da installare o selezionare un nome file dall'elenco visualizzato. Fare clic su **Apri**.

    Dopo aver aggiunto i file, nella **finestra di** dialogo Installa nuovi componenti vengono visualizzati i file aggiunti e i relativi componenti associati. Se si seleziona la **casella di** controllo Dettagli , verranno visualizzate altre informazioni sul contenuto del file e sui componenti trovati.

    > [!Note]  
    > I componenti COM non configurati devono avere una libreria dei tipi. Se COM+ non riesce a trovare la libreria dei tipi del componente, il componente non verrà visualizzato nell'elenco. È anche possibile rimuovere un file **dall'elenco File da** installare selezionandolo e facendo clic su **Rimuovi**.

     

8.  Fare **clic su** Avanti e quindi su **Fine** per installare il componente.

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

 

 



