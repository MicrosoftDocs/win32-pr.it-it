---
description: Specifica un percorso di file che rappresenta una posizione di archiviazione che può essere usata dal modulo di decrittografia del contenuto per i dati specifici del contenuto.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526899"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>\_ \_ Proprietà INPRIVATESTOREPATH di MF CONTENTDECRYPTIONMODULE

Specifica un percorso di file che rappresenta una posizione di archiviazione che può essere usata dal modulo di decrittografia del contenuto per i dati specifici del contenuto.


## <a name="data-type"></a>Tipo di dati

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID proprietà

**MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH**

## <a name="property-value"></a>Valore proprietà

Percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può usare per i dati specifici del contenuto.

## <a name="remarks"></a>Commenti

L'app deve eliminare il percorso dell'archivio dopo che l'oggetto CDM è stato rilasciato.

Se questa proprietà non è impostata, il sistema utilizzerà il percorso specificato con la proprietà [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) per i dati specifici del contenuto.

Impostare questa proprietà quando si crea un CDM chiamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Aggiornamento di Windows 10 aprile 2020<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

- [Proprietà Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




