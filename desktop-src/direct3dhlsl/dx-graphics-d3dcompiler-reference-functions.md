---
title: Funzioni del compilatore (informazioni di riferimento su HLSL)
description: Questa sezione contiene informazioni sulle funzioni del compilatore HLSL Direct3D seguenti
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- funzioni, compilatore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e9bc933baa1df3fb6d916bd37e832f58dc385bae297a2267248c8e61954a05b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673671"
---
# <a name="compiler-functions-hlsl-reference"></a>Funzioni del compilatore (informazioni di riferimento su HLSL)

Questa sezione contiene informazioni sulle funzioni del compilatore HLSL Direct3D seguenti:

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br/></td>
<td>Ottiene un puntatore a un'interfaccia di reflection.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br/></td>
<td>Compilare il codice HLSL o un file di effetto in bytecode per una determinata destinazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br/></td>
<td>Compila il codice HLSL (High Level Shader Language) Microsoft in bytecode per una determinata destinazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
È possibile usare questa API per sviluppare le app di Windows Store, ma non nelle app inviate a Windows Store. Vedere la sezione &quot; Compilazione di shader per UWP nelle note per &quot; <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2.</strong></a>
</blockquote>
<br/> Compila il codice HLSL in bytecode per una determinata destinazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
È possibile usare questa API per sviluppare le app di Windows Store, ma non nelle app inviate a Windows Store.
</blockquote>
<br/> Comprime un set di shader in un formato più compatto. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br/></td>
<td>Crea un buffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br/></td>
<td>Crea un'interfaccia function-linking-graph. <br/>
<blockquote>
[!Note]<br />
Questa funzione fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br/></td>
<td>Crea un'interfaccia del linker. <br/>
<blockquote>
[!Note]<br />
Questa funzione fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
È possibile usare questa API per sviluppare le app di Windows Store, ma non nelle app inviate a Windows Store.
</blockquote>
<br/> Decomprime uno o più shader da un set compresso. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br/></td>
<td>Disassembla il codice HLSL compilato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br/></td>
<td>Disassembla il codice HLSL compilato da un effetto Direct3D10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br/></td>
<td>Disassembla una sezione del codice HLSL compilato specificato dai passaggi di traccia dello shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br/></td>
<td>Disassembla un'area specifica di codice HLSL compilato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br/></td>
<td>Recupera una parte specifica da un risultato di compilazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
È possibile usare questa API per sviluppare le app di Windows Store, ma non nelle app inviate a Windows Store.
</blockquote>
<br/> Ottiene le informazioni di debug dello shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> può essere modificato o non disponibile per le versioni dopo l'Windows 8.1. Usare invece <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart con</strong></a> <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> valore.
</blockquote>
<br/> Ottiene le firme di input e output da un risultato di compilazione.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> può essere modificato o non disponibile per le versioni dopo Windows 8.1. Usare invece <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> con <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> valore.
</blockquote>
<br/> Ottiene la firma di input da un risultato di compilazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> può essere modificato o non disponibile per le versioni dopo l'Windows 8.1. Usare invece <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> con <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>il D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> predefinito.
</blockquote>
<br/> Ottiene la firma di output da un risultato di compilazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br/></td>
<td>Recupera gli offset dei byte per le istruzioni all'interno di una sezione del codice dello shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br/></td>
<td>Crea un'interfaccia del modulo shader dai dati di origine per il modulo shader. <br/>
<blockquote>
[!Note]<br />
Questa funzione fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br/></td>
<td>Pre-elabora il codice HLSL non ricompilato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
È possibile usare questa API per sviluppare le app di Windows Store, ma non nelle app inviate a Windows Store.
</blockquote>
<br/> Legge un file su disco in memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br/></td>
<td>Ottiene un puntatore a un'interfaccia di reflection.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>Libreria D3DReflect</strong></a><br/></td>
<td>Crea un'interfaccia di reflection della libreria dai dati di origine che contiene una libreria HLSL di funzioni. <br/>
<blockquote>
[!Note]<br />
Questa funzione fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br/></td>
<td>Imposta le informazioni in un risultato di compilazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br/></td>
<td>Rimuove i BLOB indesiderati da un risultato di compilazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
È possibile usare questa API per sviluppare le app di Windows Store, ma non nelle app inviate a Windows Store.
</blockquote>
<br/> Scrive un BLOB di memoria in un file su disco.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su D3DCompiler](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

