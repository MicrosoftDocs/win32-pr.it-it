---
title: Struttura FORMATETC
description: La struttura FORMATETC è un formato degli Appunti generalizzato, ottimizzato per includere un dispositivo di destinazione, un aspetto o una visualizzazione dei dati e un supporto di archiviazione.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730543"
---
# <a name="the-formatetc-structure"></a>Struttura FORMATETC

La struttura FORMATETC è un formato degli Appunti generalizzato, ottimizzato per includere un dispositivo di destinazione, un *aspetto* o una visualizzazione dei dati e un supporto di archiviazione. Un consumer di dati, ad esempio un'applicazione contenitore OLE, passa la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) come argomento nelle chiamate a [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) per indicare il tipo di dati desiderato da un'origine dati, ad esempio un oggetto documento composto. L'origine usa la struttura **FORMATETC** per descrivere i formati che è in grado di fornire.

[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) può descrivere praticamente tutti i dati, inclusi altri oggetti, ad esempio moniker. Un contenitore può chiedere a uno dei suoi oggetti incorporati di elencare i formati di dati chiamando [**IDataObject:: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), che restituisce un oggetto enumeratore che implementa l'interfaccia [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . Anziché rispondere semplicemente che contiene "testo e una bitmap", l'oggetto può fornire una descrizione dettagliata dei dati, tra cui il dispositivo (normalmente lo schermo o la stampante) per cui viene eseguito il rendering, l'aspetto da presentare all'utente (contenuto completo, anteprima, icona o formattato per la stampa) e il supporto di archiviazione contenente i dati (memoria globale, file su disco, oggetto di archiviazione). , o flusso). Questa possibilità di descrivere in modo accurato i dati, nel tempo, comporterà una maggiore qualità di stampa e output dello schermo, oltre a una maggiore efficienza nell'esplorazione dei dati, in cui uno sketch di anteprima è molto più veloce da recuperare e visualizzare rispetto a un rendering completamente dettagliato.

Nella tabella seguente sono elencati i campi della struttura di dati [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e le informazioni specificate.



| Campo                   | Specifica                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | Formato in cui eseguire il rendering dei dati, che può essere un formato degli Appunti standard, un formato proprietario o un formato OLE. Per ulteriori informazioni sui formati OLE, vedere [documenti composti](compound-documents.md).<br/>                                          |
| **PTD**<br/>      | Struttura [**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) , che contiene informazioni sufficienti su un dispositivo di destinazione Windows, ad esempio una schermata o una stampante, in modo che sia possibile creare un handle per il relativo contesto di dispositivo (HDC) utilizzando la funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . <br/> |
| **dwAspect**<br/> | Aspetto o visualizzazione dei dati di cui eseguire il rendering. può essere il contenuto completo, uno schizzo di anteprima, un'icona o formattato per la stampa.<br/>                                                                                                                                  |
| **Lindex**<br/>   | Parte dell'aspetto di interesse. per la presente, il valore deve essere-1, a indicare che l'intera vista è di interesse.<br/>                                                                                                                                |
| **TYMED**<br/>    | Supporto di archiviazione dei dati, che può essere una memoria globale, un file su disco o un'istanza di una delle interfacce di archiviazione strutturata di COM.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati di dati e supporti di trasferimento](data-formats-and-transfer-media.md)
</dt> </dl>

 

