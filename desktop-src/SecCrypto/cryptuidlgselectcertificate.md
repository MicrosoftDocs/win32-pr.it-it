---
description: Visualizza una finestra di dialogo che consente a un utente di selezionare un certificato.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate (funzione)
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 65d9993cd1e035473e731056d33b7a391ef47b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233691"
---
# <a name="cryptuidlgselectcertificate-function"></a>CryptUIDlgSelectCertificate (funzione)

La funzione **CryptUIDlgSelectCertificate** Visualizza una finestra di dialogo che consente a un utente di selezionare un certificato.

## <a name="syntax"></a>Sintassi


```C++
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PCSC* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CRYPTUI \_ SELECTCERTIFICATE \_ struct**](cryptui-selectcertificate-struct.md) che contiene informazioni sulla finestra di dialogo da visualizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Puntatore a una struttura [**del \_ contesto**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) del certificato che rappresenta il certificato selezionato dall'utente. Al termine dell'utilizzo di questo certificato, è necessario passare questo puntatore alla funzione [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) per decrementare il conteggio dei riferimenti del contesto del certificato.

Se il membro **dwFlags** della struttura *PCSC* non contiene il flag **CRYPTUI \_ SELECTCERT \_ MultiSelect** , il valore restituito **null** indica che l'utente ha chiuso la finestra di dialogo senza selezionare un certificato.

Se il membro **dwFlags** della struttura *PCSC* contiene il flag **CRYPTUI \_ SELECTCERT \_ MultiSelect** , questa funzione restituisce sempre **null**. I certificati selezionati saranno contenuti nell'archivio certificati rappresentato dal membro **hSelectedCertStore** di *PCSC*. Se il numero di certificati nell'archivio è uguale prima e dopo la chiamata di **CryptUIDlgSelectCertificate**, l'utente ha chiuso la finestra di dialogo senza selezionare alcun certificato.

## <a name="remarks"></a>Commenti

Se il membro **dwFlags** della struttura [**\_ \_ struct CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) è impostato su **CRYPTUI \_ SELECTCERT \_ legacy**, viene visualizzata la finestra di dialogo legacy. In caso contrario, verrà visualizzata la finestra di dialogo di selezione del certificato corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                              |
| Fine del supporto<br/> | \[Solo app desktop di Windows 7\]<br/>                                                       |
| Libreria<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Nomi Unicode e ANSI<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) e **CryptUIDlgSelectCertificateA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_struct CRYPTUI SELECTCERTIFICATE \_**](cryptui-selectcertificate-struct.md)
</dt> </dl>

�

�




