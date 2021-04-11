---
description: Elenco di URL a cui l'origine di rete invierà le informazioni di registrazione.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: Proprietà MFNETSOURCE_LOGURL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129782"
---
# <a name="mfnetsource_logurl-property"></a>\_Proprietà LogURL di MFNETSOURCE

Elenco di URL a cui l'origine di rete invierà le informazioni di registrazione.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Matrice di stringhe di caratteri wide (**CALPWSTR**)

VT \_ vettore \| VT \_ LPWSTR

**CALPWSTR**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ LogURL** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




