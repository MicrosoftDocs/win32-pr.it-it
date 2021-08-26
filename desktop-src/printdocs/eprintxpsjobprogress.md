---
description: Specifica le attività attualmente in corso dello spooler durante l'elaborazione di un processo di stampa XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Enumerazione EPrintXPSJobProgress (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef3d72d983388c022afbb0e914f87a17587f70b8e175dd57dabcd61d224e93bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949641"
---
# <a name="eprintxpsjobprogress-enumeration"></a>Enumerazione EPrintXPSJobProgress

Specifica le attività attualmente in corso dello spooler durante l'elaborazione di un processo di stampa XPS.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**
</dt> <dd>

Una sequenza di documenti sta per essere aggiunta al processo XPS.

</dd> <dt>

<span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**
</dt> <dd>

È stata aggiunta una sequenza di documenti al processo XPS.

</dd> <dt>

<span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**
</dt> <dd>

Un documento fisso sta per essere aggiunto al processo XPS.

</dd> <dt>

<span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**
</dt> <dd>

È stato aggiunto un documento fisso al processo XPS.

</dd> <dt>

<span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**
</dt> <dd>

Una pagina sta per essere aggiunta al processo XPS.

</dd> <dt>

<span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**
</dt> <dd>

È stata aggiunta una pagina al processo XPS.

</dd> <dt>

<span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**
</dt> <dd>

È stata aggiunta una risorsa al processo XPS.

</dd> <dt>

<span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**
</dt> <dd>

È stato aggiunto un tipo di carattere al processo XPS.

</dd> <dt>

<span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**
</dt> <dd>

Un'immagine è stata aggiunta al processo XPS.

</dd> <dt>

<span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**
</dt> <dd>

È stato eseguito il commit dei dati per il processo XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata principalmente come parametro per la [**funzione ReportJobProcessingProgress.**](reportjobprocessingprogress.md)

Questi valori possono fare riferimento alla fase di spooling o di rendering di un processo di stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |



 

 




