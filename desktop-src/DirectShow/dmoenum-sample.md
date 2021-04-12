---
description: Esempio DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Esempio DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225475"
---
# <a name="dmoenum-sample"></a>Esempio DMOEnum

## <a name="description"></a>Descrizione

Questa applicazione di esempio enumera tutti gli [oggetti multimediali DirectX](directx-media-objects.md) (DMOS) registrati nel sistema dell'utente e visualizza le relative informazioni.

Nell'esempio vengono utilizzate la funzione [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) e l'interfaccia [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) per enumerare DMOS. Usa l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) e altre interfacce DMO per recuperare le informazioni su ogni DMO.

## <a name="usage"></a>Utilizzo

Quando l'applicazione viene avviata, enumera tutti i DMOs installati. Se si seleziona una categoria DMO specifica, nell'applicazione vengono visualizzati solo i DMOs di tale categoria. Per visualizzare le informazioni su un DMO, selezionare DMO dall'elenco. L'applicazione Visualizza il numero di flussi, i tipi di supporto preferiti, il server DLL per tale DMO e altre informazioni su DMO. Per includere o escludere DMOs con chiave, impostare la casella di controllo **Includi DMOS?** .

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ SDK \] radice* \\ esempi \\ multimediali \\ DirectShow \\ varie \\ DMOEnum.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



