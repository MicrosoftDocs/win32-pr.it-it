---
description: Utilizzato per configurare i componenti di CAPICOM.
title: Oggetto Settings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330022"
---
# <a name="settings-object-cryptography"></a>Oggetto Settings (Cryptography)

\[L'oggetto **Impostazioni** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

L'oggetto **Settings** viene usato per configurare i componenti di CAPICOM.

## <a name="members"></a>Membri

L'oggetto **Settings** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **Settings** dispone di queste proprietà.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Proprietà</th>
<th style="text-align: left;">Tipo di accesso</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Imposta o Recupera il percorso di ricerca Active Directory. Per impostazione predefinita, la posizione iniziale non è specificata. Quando il percorso non è specificato, viene eseguita la ricerca nel catalogo globale, quindi viene eseguita la ricerca nel dominio predefinito. La ricerca determina se l'attributo del certificato utente viene pubblicato in quel percorso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Imposta o recupera un valore booleano che indica se è possibile utilizzare i prompt dell'interfaccia utente per l'identità di un firmatario o di un mittente. <br/>
<blockquote>
[!Note]<br />
L'impostazione di questa proprietà non disabilita gli avvisi generati prima che l'utilizzo della chiave privata venga eseguito da un'applicazione basata sul Web.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **Settings** ed è sicuro per lo scripting. Il ProgID per l'oggetto **Settings** è capicom. Settings. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 




