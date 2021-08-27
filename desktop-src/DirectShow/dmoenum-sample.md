---
description: Esempio di DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Esempio di DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fc51cc45ad879ccbc5ccd232b782e4b9f5511071d8d2492c135efcb322969c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079201"
---
# <a name="dmoenum-sample"></a>Esempio di DMOEnum

## <a name="description"></a>Descrizione

Questa applicazione di esempio enumera tutti gli [oggetti multimediali DirectX](directx-media-objects.md) (DMO) registrati nel sistema dell'utente e visualizza informazioni su di essi.

L'esempio usa [**la funzione DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) e [**l'interfaccia IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) per enumerare le DMO. Usa [**l'interfaccia IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) e altre interfacce DMO per recuperare informazioni su ogni DMO.

## <a name="usage"></a>Utilizzo

All'avvio dell'applicazione, enumera tutte le DMO installate. Se si seleziona una categoria DMO, l'applicazione visualizza solo le DMO in tale categoria. Per visualizzare informazioni su un DMO, selezionare la DMO dall'elenco. L'applicazione visualizza il numero di flussi, i tipi di supporti preferiti, il server DLL per tale DMO e altre informazioni sul DMO. Per includere o escludere dmo con chiave, attivare o disattivare la casella di controllo Includi **DMO con chiave?** .

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ SDK Root \]* Samples Multimedia DirectShow \\ \\ \\ \\ Misc \\ DMOEnum.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



