---
title: Struttura MrmResourceIndexerMessage (MrmResourceIndexer. h)
description: Rappresenta un messaggio generato da un indicizzatore di risorse. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: E00065E6-A468-4ACD-AF89-434E4F5025A4
keywords:
- Menu struttura MrmResourceIndexerMessage e altre risorse
- Menu puntatore struttura PMrmResourceIndexerMessage e altre risorse
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessage
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073c4f74852d341d7f0711a34abe4459dcbaa79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963897"
---
# <a name="mrmresourceindexermessage-structure"></a>Struttura MrmResourceIndexerMessage

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Rappresenta un messaggio generato da un indicizzatore di risorse. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MrmResourceIndexerMessage {
  MrmResourceIndexerMessageSeverity severity;
  ULONG                             id;
  PCWSTR                            text;
} MrmResourceIndexerMessage, *PMrmResourceIndexerMessage;
```



## <a name="members"></a>Members

<dl> <dt>

**severity**
</dt> <dd>

Tipo: **[ **MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)**

</dd> <dd>

Valore che indica la gravità del messaggio.

</dd> <dt>

**id**
</dt> <dd>

Tipo: **ULONG**

</dd> <dd>

Identificatore univoco del messaggio.

</dd> <dt>

**text**
</dt> <dd>

Tipo: **PCWSTR**

</dd> <dd>

Testo del messaggio. Non liberare questo puntatore; la memoria è di proprietà del sistema operativo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1803 \[\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

