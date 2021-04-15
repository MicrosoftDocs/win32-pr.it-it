---
description: Specifica un percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può utilizzare per l'inizializzazione.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485220"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>\_ \_ Proprietà STOREPATH di MF CONTENTDECRYPTIONMODULE

Specifica un percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può utilizzare per l'inizializzazione.


## <a name="data-type"></a>Tipo di dati

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID proprietà

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>Valore proprietà

Percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può utilizzare per l'inizializzazione.

## <a name="remarks"></a>Commenti

Il percorso specificato con questa proprietà verrà usato anche per i dati specifici del contenuto se la proprietà [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) non è impostata.

Per migliorare le prestazioni COM, l'app non deve eliminare il percorso dell'archivio dopo che l'oggetto CDM è stato rilasciato.



Impostare questa proprietà quando si crea un CDM chiamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Aggiornamento di Windows 10 aprile 2020<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

- [Proprietà Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




