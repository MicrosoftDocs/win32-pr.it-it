---
description: Gli elementi Windows Image Acquisition (WIA) 2,0 sono raggruppati in categorie che definiscono la modalità di trattamento o di utilizzo di un IWiaItem2.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUID della categoria di elementi WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307300"
---
# <a name="wia-20-item-category-guids"></a>GUID categoria elemento WIA 2,0

Gli elementi Windows Image Acquisition (WIA) 2,0 sono raggruppati in categorie che definiscono la modalità di trattamento o di utilizzo di un [**IWiaItem2**](-wia-iwiaitem2.md) . Se, ad esempio, l'elemento rappresenta un feeder, l'applicazione deve prevedere che contenga le proprietà richieste del feed di documenti e funzioni come un feeder di documenti. Se l'elemento rappresenta un file terminato, un'applicazione WIA 2,0 dovrebbe gestirla in questo modo, supponendo che i dati siano statici e presenti sul dispositivo. (Le regole per ogni elemento verranno definite nei singoli documenti delle specifiche). Ogni categoria ha una costante di tipo GUID.



| Costante                                                                                                                                                                                               | Descrizione                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <dt>**\_categoria WIA \_ auto**</dt> </dl>                             | Elemento che rappresenta le impostazioni di configurazione automatica per un dispositivo scanner WIA 2,0 che supporta l'analisi configurata automaticamente.<br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <dt>**\_feed di categoria WIA \_**</dt> </dl>                       | Elemento del feeder che è un'origine dati programmabile e segue le regole standard e i set di proprietà necessari per supportare i feed di documenti.<br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <dt>**\_feeder di categoria WIA \_ \_**</dt> </dl>       | Origine dati programmabile che descrive l'origine dati di back-side di un elemento del feeder di base duplex.<br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <dt>**\_ \_ primo feed di categoria \_ WIA**</dt> </dl>    | Origine dati programmabile che descrive l'origine dati del lato anteriore di un elemento del feeder di base duplex.<br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <dt>**\_film di categoria WIA \_**</dt> </dl>                             | Un elemento di film che è un'origine dati programmabile e segue le regole standard e i set di proprietà necessari per supportare le unità di analisi dei film.<br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <dt>**\_file di categoria \_ completato \_ WIA**</dt> </dl> | Un elemento che non è un'origine dati programmabile o un elemento che fornisce dati in un formato di file finito o un elemento cartella che contiene gli elementi del formato di file completati.<br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <dt>**\_categoria WIA \_ piana**</dt> </dl>                    | Un elemento piano che rappresenta un'origine dati programmabile e segue le regole standard e i set di proprietà necessari per supportare l'analisi con piastra piana.<br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <dt>**\_cartella di categoria WIA \_**</dt> </dl>                       | Elemento di archiviazione di cartelle (non un'origine dati programmabile) che contiene altri elementi di cartella o file finiti o entrambi.<br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <dt>**\_radice categoria \_ WIA**</dt> </dl>                             | Elemento radice per il dispositivo. <br/>                                                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




