---
title: Struttura FORMATETC
description: La struttura FORMATETC è un formato degli Appunti generalizzato, migliorato per includere un dispositivo di destinazione, un aspetto o una visualizzazione dei dati e un supporto di archiviazione.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4048b64c8b8d91abf42d43d558d103a2bfd827016c5670c17a082a7ab1fdc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103722"
---
# <a name="the-formatetc-structure"></a>Struttura FORMATETC

La struttura FORMATETC è un formato degli Appunti generalizzato,  migliorato per includere un dispositivo di destinazione, un aspetto o una visualizzazione dei dati e un supporto di archiviazione. Un consumer di dati, ad esempio un'applicazione contenitore OLE, passa la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) come argomento nelle chiamate a [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) per indicare il tipo di dati da un'origine dati, ad esempio un oggetto documento composto. L'origine usa **la struttura FORMATETC** per descrivere i formati che può fornire.

[**FORMATETC può**](/windows/win32/api/objidl/ns-objidl-formatetc) descrivere praticamente tutti i dati, inclusi altri oggetti, ad esempio moniker. Un contenitore può chiedere a uno dei relativi oggetti incorporati di elencare i formati di dati chiamando [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), che restituisce un oggetto enumeratore che implementa [**l'interfaccia IEnumFORMATETC.**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) Invece di rispondere semplicemente che ha "testo e bitmap", l'oggetto può fornire una descrizione dettagliata dei dati, tra cui il dispositivo (in genere schermo o stampante) di cui viene eseguito il rendering, l'aspetto da presentare all'utente (contenuto completo, anteprima, icona o formattato per la stampa) e il supporto di archiviazione contenente i dati (memoria globale,  file su disco, oggetto di archiviazione o flusso). Questa possibilità di descrivere in modo stretto i dati, nel tempo, comporta un output di stampa e schermo di qualità superiore, nonché una maggiore efficienza nell'esplorazione dei dati, in cui uno sketch di anteprima è molto più veloce da recuperare e visualizzare rispetto a un rendering completamente dettagliato.

Nella tabella seguente sono elencati i campi della struttura di dati [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e le informazioni specificate.



| Campo                   | Specifica                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | Formato in cui eseguire il rendering dei dati, che può essere un formato degli Appunti standard, un formato proprietario o un formato OLE. Per altre informazioni sui formati OLE, vedere [Documenti composti](compound-documents.md).<br/>                                          |
| **Ptd**<br/>      | Struttura [**DVTARGETDEVICE,**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) che contiene informazioni sufficienti su un dispositivo di destinazione Windows, ad esempio uno schermo o una stampante, in modo che sia possibile creare un handle per il contesto di dispositivo (hDC) usando la [**funzione CreateDC.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) <br/> |
| **Dwaspect**<br/> | Aspetto o visualizzazione dei dati di cui eseguire il rendering. può essere il contenuto completo, uno sketch di anteprima, un'icona o formattato per la stampa.<br/>                                                                                                                                  |
| **Lindex**<br/>   | Parte dell'aspetto di interesse; Per il momento, il valore deve essere -1, a indicare che l'intera visualizzazione è di interesse.<br/>                                                                                                                                |
| **Tymed**<br/>    | Supporto di archiviazione dei dati, che può essere memoria globale, file su disco o un'istanza di una delle interfacce di archiviazione strutturata di COM.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati di dati e supporti di trasferimento](data-formats-and-transfer-media.md)
</dt> </dl>

 

