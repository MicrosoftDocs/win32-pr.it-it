---
description: Visualizza una finestra di dialogo che consente a un utente di selezionare un certificato.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Funzione CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: fb37eb664841331ce3f37e9ce37ca3ab9e5c0f92c254cff0896c6c682a9f2872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768164"
---
# <a name="cryptuidlgselectcertificate-function"></a>Funzione CryptUIDlgSelectCertificate

La **funzione CryptUIDlgSelectCertificate** visualizza una finestra di dialogo che consente a un utente di selezionare un certificato.

## <a name="syntax"></a>Sintassi


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcsc* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ \_ STRUCT CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) che contiene informazioni sulla finestra di dialogo da visualizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Puntatore a una [**struttura CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) che rappresenta il certificato selezionato dall'utente. Al termine dell'uso di questo certificato, è necessario passare questo puntatore alla funzione [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) per decrementare il conteggio dei riferimenti del contesto del certificato.

Se il **membro dwFlags** della struttura *pcsc* non contiene il flag **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** un valore restituito **NULL** indica che l'utente ha chiuso la finestra di dialogo senza selezionare un certificato.

Se il **membro dwFlags** della *struttura pcsc* contiene il flag **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** questa funzione restituisce sempre **NULL.** I certificati selezionati saranno contenuti nell'archivio certificati rappresentato dal membro **hSelectedCertStore** di *pcsc*. Se il numero di certificati nell'archivio è lo stesso prima e dopo la chiamata di **CryptUIDlgSelectCertificate,** l'utente ha chiuso la finestra di dialogo senza selezionare alcun certificato.

## <a name="remarks"></a>Commenti

Se il **membro dwFlags** della struttura [**\_ \_ STRUCT CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) è impostato su **CRYPTUI \_ SELECTCERT \_ LEGACY,** viene visualizzata la finestra di dialogo legacy. In caso contrario, viene visualizzata la finestra di dialogo di selezione del certificato corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows solo \[ app desktop XP\]<br/>                                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                              |
| Fine del supporto<br/> | Windows 7 \[ app desktop\]<br/>                                                       |
| Libreria<br/>                  | <dl> <dt>Cryptui.lib</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Nomi Unicode e ANSI<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) e **CryptUIDlgSelectCertificateA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**](cryptui-selectcertificate-struct.md)
</dt> </dl>






