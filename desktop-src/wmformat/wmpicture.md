---
title: WM/immagine
description: L'attributo WM/Picture contiene un'immagine relativa al contenuto.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- WM/Picture formato Windows Media
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955948"
---
# <a name="wmpicture"></a>WM/immagine

L'attributo **WM/Picture** contiene un'immagine relativa al contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMPicture

## <a name="data-type"></a>Tipo di dati

[**WM \_ PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ \_ Binary di tipo WMT**)

## <a name="remarks"></a>Commenti

Questo attributo è compatibile con il frame ID3, APIC. La specifica ID3 per il frame APIC stabilisce che, mentre può essere presente un numero qualsiasi di frame APIC associati a un file, solo uno può essere di tipo 1 e solo uno può essere di tipo 2. La specifica indica inoltre che la descrizione dell'immagine non può contenere più di 64 caratteri, ma può essere vuota.

Gli attributi WM/Picture aggiunti con gli oggetti di Windows Media Format SDK non vengono convalidati automaticamente per essere conformi alle specifiche ID3. È necessario aggiungere il codice nell'applicazione per eseguire le convalide se si desidera mantenere la compatibilità completa con ID3.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> <dt>

[**immagine di WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




